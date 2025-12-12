<template>
    <div class="container">
        <div class="row">
            <h3 class="text-center">게시판</h3>
            <table class="table">
                <tbody>
                    <tr>
                        <th width="20%" class="text-center danger">번호</th>
                        <td width="30%" class="text-center" v-text="vo.no"></td>
                        <th width="20%" class="text-center danger">작성일</th>
                        <td width="30%" class="text-center" v-text="vo.dbday"></td>
                    </tr>
                    <tr>
                        <th width="20%" class="text-center danger">이름</th>
                        <td width="30%" class="text-center" v-text="vo.name"></td>
                        <th width="20%" class="text-center danger">조회수</th>
                        <td width="30%" class="text-center" v-text="vo.hit"></td>
                    </tr>
                    <tr>
                        <th width="20%" class="text-center danger">제목</th>
                        <td colspan="3" v-text="vo.subject"></td>
                    </tr>
                    <tr>
                        <td colspan="4" class="text-left" valign="top" height="250">
                            <pre style="white-space: pre-wrap;background: white; border: none;">{{ vo.content }}</pre>
                        </td>
                    </tr>
                    <tr>
                        <td colspan="4" class="text-right">
                            <a href="#" class="btn btn-xs btn-info">수정</a>
                            <a href="#" class="btn btn-xs btn-warning">삭제</a>
                            <button type="button" class="btn btn-xs btn-success" @click="goList()">목록</button>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
    <!-- <div class="container">
        <div class="row">
            <h1 class="text-center">선택된 게시물 : {{ no }}</h1>
        </div>
    </div> -->
</template>

<script setup>
import { onMounted, computed } from 'vue';
import { useStore } from 'vuex';
import { useRoute, useRouter } from 'vue-router';
const route = useRoute()
const router = useRouter()
// const no = route.params.no
const store = useStore()
const vo = computed(() => store.state.boards.board_detail)
onMounted(() => {
    store.dispatch("boards/boardDetailData", route.params.no)
})

const goList = () => {
    router.push('/board/list')
}


</script>

<style scoped>
.row {
    margin: 0px auto;
    width: 960px;
}
</style>