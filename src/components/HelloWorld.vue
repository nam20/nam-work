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
            :href="saraminUrl"
            target="_blank"
            >사람인</v-btn>
            <v-btn
            class="ma-2"
            :href="jobKoreaUrl"
            target="_blank"
            >잡코리아</v-btn>
            <v-btn
            class="ma-2"
            :href="workmmaCompany"
            target="_blank"
            >병역업체</v-btn>
            <v-btn
            class="ma-2"
            :href="workmmaRecruit"
            target="_blank"
            >병역채용</v-btn>

            <v-btn
            class="ma-2"
            :href="rocketUrl"
            target="_blank"
            >로켓펀치</v-btn>
            <v-btn
            class="ma-2"
            :href="wantedUrl"
            target="_blank"
            >원티드</v-btn>
            <v-btn
            class="ma-2"
            :href="incruitUrl"
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
            :href="worknetUrl"
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
            <v-btn
            class="ml-10"
            @click="searchClear">
              지우기
            </v-btn>
            
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
    computed:{
      jobKoreaUrl(){
        return this.search !== '' ? `http://www.jobkorea.co.kr/Search/?stext=${this.search}` : `http://www.jobkorea.co.kr/recruit/joblist?menucode=search&local=I000,B000&jobtype=9`
      },
      saraminUrl(){
        return this.search !== '' ? `http://www.saramin.co.kr/zf_user/search?search_area=main&search_done=y&search_optional_item=n&searchType=default_mysearch&searchword=${this.search}`
          : 'http://www.saramin.co.kr/zf_user/search?loc_mcd=101000%2C102000&job_type=3&company_cd=0%2C1%2C2%2C3%2C4%2C5%2C6%2C7%2C9%2C10&exc_keyword=%EC%A0%84%EB%AC%B8%EC%97%B0%EA%B5%AC%EC%9A%94%EC%9B%90&panel_type=&search_optional_item=y&search_done=y&panel_count=y'
      },
      rocketUrl(){
        return this.search !== '' ? `https://www.rocketpunch.com/search?keywords=${this.search}` : 'https://www.rocketpunch.com/jobs?hiring_types=3'
      },
      wantedUrl(){
        return this.search !== '' ? `https://www.wanted.co.kr/search?query=${this.search}` : 'https://www.wanted.co.kr/search?query=%EC%82%B0%EC%97%85%EA%B8%B0%EB%8A%A5%EC%9A%94%EC%9B%90'
      },
      incruitUrl(){
        return this.search !== '' ? `https://search.incruit.com/list/search.asp?col=job&src=gsw*search&kw=${this.search}` : 'https://job.incruit.com/jobdb_list/searchjob.asp?jobty=3&rgn2=11&rgn2=18&occ1=150'
      },
      worknetUrl(){
        return this.search !== '' ? `https://www.work.go.kr/wnSearch/unifSrch.do?regDateStdt=&regDateEndt=&colName=tb_workinfo&srchDateSelected=all&sortField=RANK&sortOrderBy=DESC&searchDateInfo=&temp=&pageIndex=1&tabName=tb_workinfo&dtlSearch=&query=${this.search}&radio_period=on&srchStdt=&srchEndt=&reQuery=&agreeQuery=&prikeyQuery=&exceptQuery=`
          : 'https://www.work.go.kr/empInfo/empInfoSrch/list/dtlEmpSrchList.do?careerTo=&keywordJobCd=&occupation=&rot2WorkYn=&templateInfo=&payGbn=&resultCnt=10&keywordJobCont=&cert=&cloDateStdt=&moreCon=&minPay=&codeDepth2Info=11000&isChkLocCall=&sortFieldInfo=DATE&major=&resrDutyExcYn=&sortField=DATE&staArea=&sortOrderBy=DESC&keyword=&termSearchGbn=all&benefitSrchAndOr=O&disableEmpHopeGbn=&webIsOut=&actServExcYn=Y&keywordStaAreaNm=&maxPay=&emailApplyYn=&listCookieInfo=DTL&pageCode=&codeDepth1Info=11000&keywordEtcYn=&publDutyExcYn=&keywordJobCdSeqNo=&exJobsCd=&templateDepthNmInfo=&computerPreferential=&regDateStdt=&employGbn=&empTpGbcd=1%2C2&region=11000%2C41000&resultCntInfo=10&siteClcd=all&cloDateEndt=&sortOrderByInfo=DESC&currntPageNo=1&indArea=&careerTypes=&searchOn=Y&subEmpHopeYn=&academicGbn=&foriegn=&templateDepthNoInfo=&mealOfferClcd=&station=&moerButtonYn=Y&holidayGbn=&enterPriseGbn=all&academicGbnoEdu=noEdu&cloTermSearchGbn=all&keywordWantedTitle=&stationNm=&benefitGbn=&keywordFlag=&essCertChk=&isEmptyHeader=&depth2SelCode=&_csrf=d5596721-f1b3-49b0-aefa-28962c8a1bee&keywordBusiNm=&preferentialGbn=all&rot3WorkYn=&pfMatterPreferential=&regDateEndt=&staAreaLineInfo1=11000&staAreaLineInfo2=1&pageIndex=1&termContractMmcnt=&careerFrom=&laborHrShortYn=#viewSPL'
      },
      workmmaCompany(){
        return this.search !== '' ? `https://work.mma.go.kr/caisBYIS/search/byjjecgeomsaek.do?eopjong_gbcd=1&eopche_nm=${this.search}` : 'https://work.mma.go.kr/caisBYIS/search/byjjecgeomsaek.do?eopjong_gbcd=1&eopjong_gbcd_list=11111,11112&bjinwonym=H&sido_addr=%EC%84%9C%EC%9A%B8%ED%8A%B9%EB%B3%84%EC%8B%9C'
      },
      workmmaRecruit(){
        return this.search !== '' ? `https://work.mma.go.kr/caisBYIS/search/cygonggogeomsaek.do?eopjong_gbcd=1&eopche_nm=${this.search}` : 'https://work.mma.go.kr/caisBYIS/search/cygonggogeomsaek.do?eopjong_gbcd=1&eopjong_gbcd_list=11111,11112&yeokjong_brcd=006'
      }
      

    },
    methods:{
      searchClear(){
        this.search = ''
      }
    }
   
   
    
  }
</script>

<style scoped>

</style>