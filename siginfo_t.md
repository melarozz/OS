Структура, которая ассоциирована с отправкой сигнала
man siginfo_t
Unix профессиональное программирование (На русском) [377 +]

              typedef struct {
                  int      si_signo;  /* Signal number */
                  int      si_code;   /* Signal code */
                  pid_t    si_pid;    /* Sending process ID */
                  uid_t    si_uid;    /* Real user ID of sending process */
                  void    *si_addr;   /* Address of faulting instruction */
                  int      si_status; /* Exit value or signal */
                  union sigval si_value;  /* Signal value */
              } siginfo_t;

Хранит:
  * номер сигнала (номер, который represent имя сигнала )
  * код сигнала (Почему сигнал послан)
  * [[PID]] отправленного сигнала
  * Real [[UserID]] (связано с созданием [[core]] файла)
  * ![[Pasted image 20231226194514.png]]