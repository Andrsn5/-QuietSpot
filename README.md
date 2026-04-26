Часть приложения переписывается с другого стека, поэтому картинки могут не совпадать
## Stack

**Язык:** Kotlin
**Архитектура:** Clean Architecture (Presentation → Domain → Data)

| Слой | Технологии |
|------|------------|
| **UI** | XML Views, Material 3 |
| **State** | MVVM, RxJava 3, BehaviorSubject |
| **DI** | Dagger 2 |
| **Network** | Retrofit 2, OkHttp |
| **База данных** | Room |
| **Фоновые задачи** | WorkManager + RxWorker |
| **Build** | Gradle KTS, KAPT |

## Ключевые решения

- **Clean Architecture** — чёткое разделение на Presentation, Domain и Data слои
- **RxJava 3** — реактивные потоки данных через `Observable`, `Single`, `Completable`
- **Dagger 2** — компайл-тайм DI без рефлексии, `@Component`, `@Module`, `@Inject`
- **WorkManager + RxWorker** — фоновые задачи (скачивание) с поддержкой foreground service и уведомлений
- **Room + RxJava** — реактивная БД через `Flowable` для автоматического обновления UI

<div style="display: flex; justify-content: center; gap: 10px;">
  <img src="https://github.com/user-attachments/assets/b780d252-8a97-485c-8956-358658ece4c3"  width="30%" />
  <img src="https://github.com/user-attachments/assets/12120ad9-d2f7-42fc-b966-dfbea6c07485" width="30%" />
  <img src="https://github.com/user-attachments/assets/694a7d2d-3b8d-43ac-8d3e-d0f50cffa6d7" width="30%" />
</div>
