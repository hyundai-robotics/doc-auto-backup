# Hi6 로봇제어기 기능설명서 - 자동 백업

{% hint style="warning" %}
본 제품 설명서에서 제공되는 정보는 현대로보틱스의 자산입니다.

현대로보틱스의 서면에 의한 동의 없이 전부 또는 일부를 무단 전재 및 재배포할 수 없으며, 제3자에게 제공되거나 다른 목적에 사용할 수 없습니다.



본 설명서는 사전 예고 없이 변경될 수 있습니다.



**Copyright ⓒ 2020 by Hyundai Robotics**
{% endhint %}
# 1. 개요

# 1.1 사전지식

본 설명서를 잘 이해하기 위해서는 아래의 지식을 갖추고 있어야 합니다.

* [Hi6 로봇제어기 조작설명서](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/README)
# 1.2 자동 백업 기능에 대해서

자동 백업은 미리 설정된 조건에 의해 Hi6 제어기의 현재 프로젝트 폴더, 로그(log) 폴더 전체를 자동 혹은 수동으로 백업하는 기능 입니다. 사용자는 백업된 시점 중 하나를 선택하여 시스템을 복원할 수 있습니다. 고장 혹은 사용자 실수에 의해 Hi6 제어기의 파일이 지워지거나 손상되었을 때, 이러한 백업 데이터들이 사용됩니다.

백업을 수행하는 조건은 다음 3가지 방식으로 정할 수 있습니다.

1. 지정된 날짜와 시간 (최대 4개 설정)
2. 지정된 입력할당신호가 켜질 때
3. 수동 → 자동으로 모드가 전환될 때
# 2. 자동 백업의 사용

# 2.1 설정

`[F2: 시스템] – 2: 제어 파라미터 - 8: 자동 백업 및 복원 화면`으로 진입하십시오.

![그림. 자동 백업 및 복원 화면](<../_assets/auto-backup.png>)

`[F2: 백업]` 버튼을 누르면, 설정에 관계없이 즉시 백업이 수행됩니다.

화면의 항목들을 설정한 후 `[확인]` 버튼을 누르면, 설정값들이 저장/적용됩니다. 각 항목의 의미는 다음 표와 같습니다.

<style type="text/css">
table  {border-collapse:collapse;}
td {border-color:gray;border-style:solid;border-width:1px;}
.grayed {background-color:lightgray; color:black}
</style>

<table class="tg">
<thead>
	<tr>
		<th>
			항 목
		</th>
		<th colspan="2">
			설 명
		</th>
		<th>
			기 타
		</th>
	</tr>
</thead>	
<tbody>
	<tr>
		<td>
			자동 백업 사용
		</td>
		<td colspan="2">
			무효: 자동 백업 기능을 끄기
			유효: 자동 백업 기능을 켜기
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			최대 백업 버전수
		</td>
		<td colspan="2">
			최대 몇 개의 백업 지점을 관리할 것인지를 설정.<br /> 지정한 개수이상으로 백업이 수행될 때는 가장 오래된 백업 지점이 삭제됩니다.
		</td>
		<td>
			1~100
		</td>
	</tr>
	<tr>
		<td>
			백업 시간
		</td>
		<td colspan="2">
			매일 혹은 특정 요일의 특정 시간에 백업이 자동으로 수행되도록 설정합니다. 최대 4개의 스케줄을 입력할 수 있습니다. 사용하지 않는 스케줄은 미지정으로 선택하십시오.
		</td>
		<td>
			00:00
			~
			23:59
		</td>
	</tr>
	<tr>
		<td rowspan="4">
			모드 전환시 백업
			(수동 &agrave; 자동)
		</td>
		<td colspan="2">
			수동모드에서 자동모드로 전환되는 순간의 백업 여부를 설정합니다.
		</td>
		<td rowspan="4">
			-
		</td>
	</tr>
	<tr>
		<td>
			- 무효:
		</td>
		<td>
			백업하지 않음
		</td>
	</tr>
	<tr>
		<td>
			- 사용자 확인:
		</td>
		<td>
			사용자에게 백업할 지를 확인받는 대화상자를 표시. 예로 답하면 백업.
		</td>
	</tr>
	<tr>
		<td>
			- 확인없이:
		</td>
		<td>
			사용자 확인 대화상자를 표시하지 않고, 즉시 백업.
		</td>
	</tr>
	<tr>
		<td>
			입력할당신호
			(백업실행)
		</td>
		<td colspan="2">
			지정한 입력신호가 켜지면, 백업을 실행합니다.
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			출력할당신호
			(백업중)
		</td>
		<td colspan="2">
			백업이 수행되는 동안 지정한 출력신호가 켜집니다.
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			출력할당신호
			(백업에러)
		</td>
		<td colspan="2">
			백업 수행에 에러가 발생하면 켜집니다.
			[Reset]키를 두번 누르거나 혹은 [Reset][0][ENTER] 키를 누르면 해제됩니다.
		</td>
		<td>
			-
		</td>
	</tr>
<tbody>
</table>


할당신호의 설정값을 입력하는 예는 다음과 같습니다.

<table>
<thead>
	<tr>
		<th>
			신호 종류
		</th>
		<th>
			설정 예
		</th>
		<th>
			설정 결과
		</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td>
			논리신호 (PLC ON시)
			하드와이어드 신호 (PLC OFF시)
		</td>
		<td>
			135
		</td>
		<td>
			135 (135번 신호)
		</td>
	</tr>
	<tr>
		<td>
			필드버스
		</td>
		<td>
			5.220
		</td>
		<td>
			fb5.220 (fb5의 220번 신호)
		</td>
	</tr>
</tbody>
</table># 2.2 자동 백업의 실행

백업 조건이 만족하는 순간 백업이 실행됩니다. 설정 화면, 교시, 조그 진행 도중, 자동 모드의 로봇 재생 등 어떠한 상황에서도 백업은 수행됩니다. 단, 이미 백업이나 복원이 수행되고 있는 중에는 백업이 수행되지 않습니다.

백업 중엔 화면에 아래 그림과 같은 메시지박스가 나타납니다. 완료 메시지가 나올 때까지 조작을 멈추고 기다려주십시오.

![](<../_assets/backup_st.png>)

![그림 2.2 자동백업 메시지박스](<../_assets/backup_en.png>)

백업되는 위치는 메인보드 내의 아래 경로입니다.

<style type="text/css">
table  {border-collapse:collapse;}
td {border-color:gray;border-style:solid;border-width:1px;}
.grayed {background-color:lightgray; color:black}
</style>

<table>
	<tr>
		<td class='grayed'>
			<p>경로명</p>
		</td>
		<td>
			<p>/ata0:2/lib/hi6/backup/ts/</p>
		</td>
		<td>
			<p>파일관리자 화면에서 MAIN 항목 밑의 backup/ts/</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>생성되는 서브폴더명</p>
		</td>
		<td>
			<p>b{날짜}_{시간}의 형식</p>
		</td>
		<td>
			<p>접두어 b는 backup을 의미</p>
		</td>
	</tr>
</table>

예) MAIN/backup/ts/b20230512_1730/

메인보드의 여유공간이 10% 미만일 경우에는, 가장 오래된 백업지점을 삭제한 후 백업이 수행됩니다. 만일, 백업 중 여유공간이 모자랄 경우에는 백업이 중단됩니다.

이력 창을 열면, 백업 시작과 종료, 에러의 기록을 볼수 있습니다.
# 2.3 복원

`[F2: 시스템] – 2: 제어 파라미터 - 8: 자동 백업 및 복원` 화면으로 진입하십시오.

`[F1: 복원]` 버튼을 클릭하면, 아래와 같은 화면이 나타납니다.

![그림 복원 대화상자](../_assets/restore.png)

리스트박스에 복원 가능한 지점들이 백업한 시점을 기준으로 정렬되어 나타납니다. 가장 아래에 위치한 항목이 가장 최근의 백업 지점입니다.

* `[삭제]`: 항목을 선택한 후 누르면, 사용자의 확인을 받은 후 선택된 복원 지점을 삭제합니다.
* `[복원]`: 복원할 항목을 선택한 후 누르면, 복원이 시작됩니다.

복원이 완료되면 아래 그림과 같은 메시지가 나타납니다. 전원을 재투입하면 정상적인 사용이 가능해집니다.

![그림 2.5 복원 완료](<../_assets/restored_reboot.png>)
# 산업안전보건기준에 관한 규칙 및 안전검사 고시

당해 산업용 로봇은 산업안전보건기준에 관한 규칙 및 안전검사 고시(검사 대상일 경우)의 검사 기준을 고려하여 설치하여야 한다.

"[산업안전보건기준에 관한 규칙](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/korean/README)"
# 품질보증

"[품질보증](https://hrbook-hrc.web.app/#/view/quality-assurance/korean/README)"
