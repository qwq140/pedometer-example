## Pedometer 라이브러리 제공하는 기능
### 1. 걸음 수 스트림 제공
```dart
Stream<StepCount> stepCountStream = Pedometer.stepCountStream;
```
- 걸음 수 데이터를 스트림으로 제공하여 앱에서 걸음 수 변경을 실시간으로 감지할 수 있다.
- 걸음 수는 디바이스 부팅 후 부터의 누적 걸음 수 이다.

### 2. StepCount 클래스
- 걸음 수 데이터를 나타냄
- int steps : 걸음 수
- DateTime timeStamp : 걸음 수가 기록된 시간

### 3. 걸음 상태 스트림 제공
```dart
Stream<PedestrianStatus> pedometerStream = Pedometer.pedestrianStatusStream;
```
- 사용자가 걷고 있는 상태를 스트림으로 제공

### 4. PedestrianStatus 
- 사용자의 걷기 상태를 나타냄
- String status : 현재 상태 (walking, stopped, unknown)
- DateTime timeStamp : 상태가 변경된 시간
