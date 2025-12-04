Rozdział 3: Współpraca i zdalne repozytoria
===========================================

Aby w pełni wykorzystać potencjał Gita, musisz nauczyć się pracować ze
zdalnymi repozytoriami. Są to wersje Twojego projektu hostowane w
internecie lub innej sieci. Współpraca z innymi polega na wysyłaniu
swoich zmian do tych repozytoriów i pobieraniu zmian wprowadzonych przez
innych.

**Czym są zdalne repozytoria?**
-------------------------------

Zdalne repozytorium (ang. *remote*) to po prostu kopia repozytorium,
która znajduje się zazwyczaj na dedykowanym serwerze. Popularne serwisy
hostingowe to GitHub, GitLab czy Bitbucket. Praca ze zdalnym
repozytorium pozwala na:

-  **Backup:** Twoja praca jest bezpieczna nawet w przypadku awarii
   Twojego komputera.

-  **Współpracę:** Wiele osób może pracować nad tym samym projektem,
   synchronizując swoje zmiany za pośrednictwem centralnego serwera.

-  **Code Review:** Platformy te oferują narzędzia do przeglądu kodu
   (Pull Requests/Merge Requests) przed jego włączeniem do głównej
   gałęzi.

**Klonowanie istniejącego repozytorium**
----------------------------------------

Jeśli chcesz dołączyć do istniejącego projektu, pierwszą rzeczą, którą
zrobisz, będzie jego "sklonowanie".

.. code-block:: bash

   git clone https://github.com/uzytkownik/projekt.git

To polecenie tworzy katalog o nazwie "projekt", inicjalizuje w nim
katalog .git, pobiera wszystkie dane tego repozytorium i wypakowuje
najnowszą wersję plików.

**Synchronizacja zmian (Push & Pull)**
--------------------------------------

Po wprowadzeniu lokalnych zmian i ich zatwierdzeniu (commit), chcesz
podzielić się nimi z zespołem. Używasz do tego polecenia git push.

.. code-block:: bash

   git push origin main

Powyższe polecenie wysyła Twoją gałąź main na zdalny serwer o nazwie
origin (to domyślna nazwa nadawana serwerowi, z którego sklonowałeś
repozytorium).

Aby pobrać zmiany, które inni wysłali na serwer, używasz polecenia git
pull.

.. code-block:: bash

   git pull origin main

Jest to w rzeczywistości skrót, który wykonuje dwie operacje: najpierw
pobiera dane ze zdalnego serwera (git fetch), a następnie próbuje scalić
je z Twoją aktualną gałęzią (git merge).

**Najlepsze praktyki**
----------------------

Aby współpraca przebiegała gładko, warto stosować się do kilku zasad:

-  **Często pobieraj zmiany (pull):** Zanim zaczniesz pracę, upewnij
   się, że masz aktualną wersję kodu, aby uniknąć konfliktów.

-  **Pracuj na gałęziach (branches):** Nie wprowadzaj zmian bezpośrednio
   na głównej gałęzi (często main lub master). Twórz nowe gałęzie dla
   każdej nowej funkcji lub poprawki błędu.

-  **Pisz jasne komunikaty commitów:** Dobry opis zmiany pomaga innym
   zrozumieć, co i dlaczego zostało zrobione.

-  **Rób małe, logiczne commity:** Łatwiej jest przeglądać i ewentualnie
   wycofywać małe zmiany niż ogromne pakiety poprawek.
