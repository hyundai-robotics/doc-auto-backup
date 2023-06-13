# 2.1 설정

`[F2: 시스템] – 2: 제어 파라미터 - 8: 자동 백업 및 복원 화면`으로 진입하십시오.

![그림. 자동 백업 및 복원 화면](<../_assets/auto-backup.png>)

`[F2: 지금 백업]` 버튼을 누르면, 설정에 관계없이 즉시 백업이 수행됩니다. (자동백업 보관장소 만은 현재 저장된 설정을 따릅니다.)

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
			자동백업 보관장소
		</td>
		<td colspan="2">
			TP: 티치펜던트의 저장장치(storage)에 백업할 지 여부.<br>
			MAIN: 메인모듈(COM)의 스토리지에 백업할 지 여부.
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
			최대 몇 개의 백업 지점을 관리할 것인지를 설정.<br/> 지정한 개수이상으로 백업이 수행될 때는 가장 오래된 백업 폴더들이 삭제됩니다.
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
			매일 혹은 특정 요일의 특정 시간에 백업이 자동으로 수행되도록 설정합니다. 최대 4개의 스케줄을 입력할 수 있습니다. 사용하지 않는 스케줄은 체크를 끄십시오.
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
			지정한 입력신호가 켜지는 순간, 백업을 실행합니다.
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
			135
		</td>
		<td>
			135 (do135, 혹은 di135)
		</td>
	</tr>
	<tr>
		<td>
			5.220
		</td>
		<td>
			fb5.220 (fb5의 do220, 혹은 di220)
		</td>
	</tr>
</tbody>
</table>