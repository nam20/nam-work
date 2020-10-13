<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-card
        width="400px"
        class="mx-auto my-5 pa-5">
          <v-text-field 
          placeholder="검색"
          v-model="search"/>
        </v-card>
        <v-card
        width="800px"
        class="mx-auto my-5 pa-5">
            <v-btn
            class="ma-2"
            :href="`http://www.saramin.co.kr/zf_user/search?search_area=main&search_done=y&search_optional_item=n&searchType=default_mysearch&searchword=${search}`"
            target="_blank"
            >사람인</v-btn>
            <v-btn
            class="ma-2"
            :href="`http://www.jobkorea.co.kr/recruit/joblist?menucode=search`"
            target="_blank"
            >잡코리아</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://work.mma.go.kr/caisBYIS/search/byjjecgeomsaek.do?eopjong_gbcd=1&eopche_nm=${search}`"
            target="_blank"
            >병역일터</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://www.rocketpunch.com/jobs?hiring_types=3`"
            target="_blank"
            >로켓펀치</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://www.wanted.co.kr/search?query=${search}`"
            target="_blank"
            >원티드</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://job.incruit.com/jobdb_list/searchjob.asp?kw=%BA%B4%BF%AA%C6%AF%B7%CA&rgn2=18&rgn2=11`"
            target="_blank"
            >인크루트</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://www.jobplanet.co.kr/search?query=${search}&category=&_rs_con=companies&_rs_act=cover&_rs_element=main_search_bar`"
            target="_blank"
            >잡플래닛</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://kreditjob.com/`"
            target="_blank"
            >크레딧잡</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://www.work.go.kr/empInfo/empInfoSrch/list/dtlEmpSrchList.do?careerTo=&keywordJobCd=&occupation=&rot2WorkYn=&templateInfo=&payGbn=&resultCnt=10&keywordJobCont=&cert=&cloDateStdt=&moreCon=&minPay=&codeDepth2Info=11000&isChkLocCall=&sortFieldInfo=DATE&major=&resrDutyExcYn=&sortField=DATE&staArea=&sortOrderBy=DESC&keyword=&termSearchGbn=all&benefitSrchAndOr=O&disableEmpHopeGbn=&webIsOut=&actServExcYn=Y&keywordStaAreaNm=&maxPay=&emailApplyYn=&listCookieInfo=DTL&pageCode=&codeDepth1Info=11000&keywordEtcYn=&publDutyExcYn=&keywordJobCdSeqNo=&exJobsCd=&templateDepthNmInfo=&computerPreferential=&regDateStdt=&employGbn=&empTpGbcd=1%2C2&region=11000%2C41000&resultCntInfo=10&siteClcd=all&cloDateEndt=&sortOrderByInfo=DESC&currntPageNo=1&indArea=&careerTypes=&searchOn=Y&subEmpHopeYn=&academicGbn=&foriegn=&templateDepthNoInfo=&mealOfferClcd=&station=&moerButtonYn=Y&holidayGbn=&enterPriseGbn=all&academicGbnoEdu=noEdu&cloTermSearchGbn=all&keywordWantedTitle=&stationNm=&benefitGbn=&keywordFlag=&essCertChk=&isEmptyHeader=&depth2SelCode=&_csrf=d5596721-f1b3-49b0-aefa-28962c8a1bee&keywordBusiNm=&preferentialGbn=all&rot3WorkYn=&pfMatterPreferential=&regDateEndt=&staAreaLineInfo1=11000&staAreaLineInfo2=1&pageIndex=1&termContractMmcnt=&careerFrom=&laborHrShortYn=#viewSPL`"
            target="_blank"
            >워크넷</v-btn>
            <v-btn
            class="ma-2"
            :href="`http://search.career.co.kr/?kw=%uBCD1%uC5ED%uD2B9%uB840&page=1&sort=1&ac=&jc=&ct=&cr=&biz=&pay=`"
            target="_blank"
            >커리어</v-btn>
            <v-btn
            class="ma-2"
            :href="`https://map.naver.com/v5/search/${search}?c=14141208.4375751,4517939.0043474,15,0,0,0,dh`"
            target="_blank"
            >네이버 지도</v-btn>
            
        </v-card>
        
        
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data(){
      return {
        search: ''
      }
    },
   
   
    
  }
</script>

<style scoped>

</style>