OPTIONS, TRACE 둘다 메소드 리스트 노출될 경우

첫번째가 /conf/web.xml 에 메소드 제한 설정하는거고

두번째가 /conf/server.xml 에 allowTrace="true" 설정하는거다

 

테스트-톰캣 8.0.12, 9.0.12

디폴트로 OPTIONS, TRACE 전송 시 메소드 리스트 뜬다/conf/web.xml 에서 메소드 제한 설정 

아래줄에 <auth-constraint /> 이게 중요

이거 빼먹으면 적용 안된다/conf/server.xml 에 allowTrace="true" 해야 TRACE 날려도 메소드 리스트 안뜬다

원래 위에꺼 없이 이것만 설정하면 TRACE 활성화됨 위 두개 설정하고 재부팅하면 OPTIONS, TRACE 둘다 안먹힘~
