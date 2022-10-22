# EEScript

아이템과 스펠 사용을 제외한 편리한 발더스 게이트 여행을 위한 스크립트 입니다.  
이 스크립트는 다이얼로그를 추가, 수정하지 않고 함정 작동 스크립트만 수정하기 때문에 타 모드와의 충돌이 없습니다.  
스크립트를 이용한 아이템과 스펠 사용은 어떤 방식으로 지원을 해도 스펠과 아이템이 낭비되기 때문에 배제했습니다.  
스펠 사용이 추가된다면 아마 돌피부 같은 초장기 버프, 저장기 시리즈 같은 시간 제한 없는 스펠, 전투 전 해야하는 귀찮은 버프 스펠들을 지원할 생각입니다.  
함정 자동 해제는 일단 모드에 있는 함정을 제외하면 대부분의 함정에 적용될거라 생각하는데 충분한 테스트를 거치지 못했습니다.  
레날님의 [ScriptsAlive!](https://cafe.naver.com/nextrealm) 를 참조하여 넣은 기능으로 더 많은 함정들을 자동 해제 하게 수정하였습니다.

## 특징

* 핫키를 통해 캐릭터의 평시, 전투시 행동을 선택할 수 있습니다.
* 함정을 발견한 후 시프를 함정 근처로 보내면 자동으로 함정을 해제합니다.
  - 함정이 가까이 여러개 있을 경우 자동 해제가 되지 않을 수 있습니다. 이 때는 직접 해제를 해야 합니다.
* 성역, 투명화, 언데드 퇴치, 바드의 노래, 샤먼의 춤 도중에는 공격하지 않습니다.
* 적들 중 주문 시전자가 보이면 주문 시전자를 먼저 공격합니다. (메이지/드루이드/바드/클레릭 순)
* 전투가 끝나지 않았으나 적이 보이지 않으면 적과 전투중인 동료에게 이동합니다. (샤먼의 춤 중이면 이동하지 않음)

## 팁

* 근접 무기를 착용했으나 근접 공격을 하지 않기를 원하는 마법사는 무기 슬롯에서 원거리 무기를 제거하고 근접 무기만 착용 후 전투 모드를 원거리 모드를 선택하면 근접 공격을 하지 않습니다.
* 근접, 원거리 모드는 적을 만난 시점에 근거리 또는 원거리 무기를 착용하고 전투가 끝나기 전까지 무기 교체를 하지 않기 때문에 전투중에는 필요에 따라 직접 무기를 교체할 수 있습니다.
* 전투시 시프나 샤먼으로 환상을 제거를 원하면 항상 환상 탐지를 선택하면 공격하지 않고 환상 탐지를 계속합니다. 환상이 제거되면 다시 비 전투시 함정 찾기로 전환하여 전투를 하면 됩니다.

## 핫키

* V: 선택한 캐릭터의 인공 지능을 키고 끕니다.
* N: 전투 모드를 선택합니다.

| 전투 모드 | 설명                                                             |
| --------- | ---------------------------------------------------------------- |
| 근접      | 전투시 근접 무기로 공격합니다.                                   |
| 원거리    | 전투시 원거리 무기로 공격합니다.                                 |
| 공격      | 전투시 거리가 가까우면 근접 무기, 멀면 원거리 무기로 공격합니다. |

* B: 선택한 캐릭터가 평시 또는 전투시 해야할 행동을 선택합니다.
  - 항상 하는 행동은 전투/비전투 상관없이 항상 유지합니다.

| 직업                            | 행동 1              | 행동 2                         | 행동 3           | 행동 4           |
| ------------------------------- | ------------------- | ------------------------------ | ---------------- | ---------------- |
| 바드                            |                     | 항상 바드의 노래               |                  |                  |
| 팔라딘, 클레릭, 클/메, 파/메/클 |                     | 항상 언데드 퇴치               |                  |                  |
| 레인저                          |                     | 적이 보이지 않으면 그림자 숨기 |                  |                  |
| 클레릭/레인저                   |                     | 적이 보이지 않으면 그림자 숨기 | 항상 언데드 퇴치 |                  |
| 몽크                            | 비 전투시 함정 찾기 | 적이 보이지 않으면 그림자 숨기 |                  |                  |
| 샤먼                            | 비 전투시 함정 찾기 | 항상 샤먼의 춤                 | 항상 환상 탐지   |                  |
| 시프, 파/시, 메/시, 파/메/시    | 비 전투시 함정 찾기 | 적이 보이지 않으면 그림자 숨기 | 항상 환상 탐지   |                  |
| 클레릭/시프                     | 비 전투시 함정 찾기 | 적이 보이지 않으면 그림자 숨기 | 항상 환상 탐지   | 항상 언데드 퇴치 |
