 5 задание. Управление сессиями 


2 роли: добавляется в БД флаг bool isAdmin по умолчанию обычный пользователь, можно вручную назначить администратором.
	
После входа/регистрации отображается на главной отображается админ-панель для роли администратора. (Например, администратор может назначать обычных пользователей администраторами и обратно)
	Главная идея - разграничения доступности функционала для обычного пользователя и админа
	
Добавить управление сессиями.Установить максимальную длину сессии , после истечении отображать окно "Время жизни сессии истекло, пожалуйста авторизуйтесь" с переходом на страницу авторизации.
	
Access/Refresh token
	
Использовать object SessionManagerUtil 
	Описать fun startUserSession(context: Context, expiresIn: Int)
	fun isSessionActive(currentTime: Date,context: Context) : Boolean
	Проверяем активна ли сессия, чтобы разрешить пользователю выполнять действия
	fun endUserSession(context: Context)
	
Кнопка Выйти - окончание сессии
	private fun getExpiryDateFromPreferences(context: Context) : Long?
