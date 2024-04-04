# 분산 신원(DID) 기반 학사증명 시스템

## 개발 목표

대학교에서 학생증, 성적증명서 등의 증명서를 종이 증명 대신에 분산 신원 기반 자격 증명 형태로 학생에게 발급해주고, 학생은 이러한 자격 증명을 모바일 지갑앱을 사용하여 외부인에게 제시한다. 자격 증명을 제시받은 외부인도 모바일 지갑앱을 통하여 자격 증명을 검증한다.
이때 자격 증명 보유자는 개인 정보 유출을 최소화하기 위해 발급된 자격 증명(학생증, 성적증명서 등)에서 개인정보 일부(주민번호 등)을 가리고 제시하거나 성인 여부만 제시할 수 있다.

## 필요성

신분증이나 각종 증명서는 도장 등을 육안 검사로 진위 여부를 확인해야 하므로 각종 증명서의 형식과 직인에 대한 정확하고 세부적인 지식이 없는 일반인들은 쉽게 위조된 신분증이나 증명서에 속을 수 있다. 그리고 기존 신분증이나 증명서는 발급하고 소지하기가 불편하다.
신분증이나 증명서를 제시하면 성인 여부만 알 필요가 있는 상대(술담배&숙박업소 등)에게조차 주민번호 전체를 공개해야하는 등 개인 정보 유출 위험이 높다.

분산 신원(DID) 기술은 DPKI(Decentralized Public Key Infrastructure) 기술을 기반으로 손쉽게 신분증을 발급할 수 있고 모바일 지갑앱에 저장하기 때문에 자격 증명의 개수가 아무리 늘어도 휴대가 간편하며, 육안 검사가 아니라 모바일 지갑앱에서 공개키 기반으로 자동 검증되므로 증명서의 위변조가 사실상 불가능하고 이를 검증하는 것도 매우 용이하다. 그리고 증명서 전체 내용을 제시하지 않고 일부 정보만을 제시할 수 있어 개인 정보 유출을 최소화할 수 있다.

이 때문에 우리나라에서도 모바일 방역패스 COOV, 모바일 운전면허증이 분산 신원 기술에 기반하여 만들어졌으며, 올해부터 발급될 예정인 모바일 주민등록증도 분산 신원 기술에 기반하여 만들어질 예정이다.
도래하는 분산 신원 기술에 대비하기 위해 학생증, 성적 증명서 등 몇 가지 증명서의 발급, 보유, 제시, 검증을 지원하는 분산 신원 기반 시스템을 개발한다.

## 시스템 구성 요소 (완성되었을 때의 결과물)
 * 증명서 발급 앱: 학교 행정원이 학생증, 성적 증명서를 발급하기 위한 앱
 * 모바일 지갑 앱(혹은 웹): 발급된 학생증, 성적 증명서를 저장하고 제시하고 검증하기 위한 앱
 * VDR(Verifiable Data Registry): 자격 증명의 발급과 제시, 검증 등 전 과정에서 사용되는 공개키와 DID 도큐먼트가 저장되는 저장소. 이더리움 등 블록체인에 저장됨.

## 예상되는 문제점 및 핵심 요소
 * 분산 신원 기술은 기초적인 부분만 표준화되었고 많은 부분이 표준화되어 있지 않으며 활용할 수 있는 기술자료와 오픈소스가 풍부하지 못하다.
 * 최근 SSI Korea가 주최하는 DID 강의를 들었고, 학부 과목 네트워크최신기술에서 블록체인을 다루고 있고, 웹서버컴퓨팅도 배우고 있어서 이 과목들에서 배운 것을 활용하여 개발할 예정이다.

## 개발 방법
1. SSI Korea 포럼에서 제공한 다음 오픈소스를 활용하여 골격 시스템 구현 및 검증
- CLI 기반 DID 발급 서버
- CLI 기반 DID 자격증명 보유, 제시, 검증 클라이언트
- 이더리움 기술 기반으로 골격 시스템 업그레이드 구현 및 검증
2. 최신 이더리움 기술로 골격 시스템 업그레이드 구현 및 검증
3. DID를 학생증, 성적 증명서로 업그레이드 구축 및 검증
4. CLI 기반 시스템을 GUI 기반 시스템으로 업그레이드 구축 및 검증
