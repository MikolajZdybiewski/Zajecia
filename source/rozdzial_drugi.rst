Rozdział 2: Pierwsze kroki z Gitem
===================================

Rozpoczęcie pracy z Gitem może wydawać się skomplikowane, ale w
rzeczywistości codzienna praca opiera się na kilku podstawowych
poleceniach. Omówimy teraz fundamentalne operacje, które będziesz
wykonywać setki razy.

**Konfiguracja początkowa**
---------------------------

Zanim zaczniesz używać Gita, musisz przedstawić się systemowi. Git
dołącza te informacje do każdego zatwierdzenia (commita), które robisz.

.. code-block:: bash

        git config --global user.name "Jan Kowalski"
        git config --global user.email "jan.kowalski@example.com"

Użycie opcji --global oznacza, że ta konfiguracja będzie dotyczyć
wszystkich Twoich projektów na danym komputerze.

**Tworzenie nowego repozytorium**
---------------------------------

Aby przekształcić zwykły katalog w repozytorium Gita, należy w nim
wykonać polecenie inicjalizacji.

.. code-block:: bash

        mkdir moj-projekt cd moj-projekt git init

Polecenie git init tworzy w katalogu podkatalog .git. Zawiera on
wszystkie niezbędne pliki repozytorium – szkielet historii Twojego
projektu. W tym momencie nic jeszcze nie jest śledzone.

**Trzy stany pliku w Gicie**
----------------------------

Kluczowe dla zrozumienia Gita jest poznanie trzech głównych stanów, w
jakich mogą znajdować się Twoje pliki:

1. **Modified (Zmieniony):** Plik został zmodyfikowany w katalogu
   roboczym, ale zmiany nie zostały jeszcze zapisane w bazie danych
   Gita.

2. **Staged (W poczekalni):** Zmodyfikowany plik został oznaczony w
   swojej aktualnej wersji jako przeznaczony do włączenia do następnego
   zatwierdzenia (commita).

3. **Committed (Zatwierdzony):** Dane zostały bezpiecznie zapisane w
   Twojej lokalnej bazie danych (repozytorium).

**Podstawowy cykl pracy (Workflow)**
------------------------------------

Typowy przepływ pracy wygląda następująco:

1. Modyfikujesz pliki w swoim katalogu roboczym.

2. Używasz polecenia git add, aby przenieść wybrane zmiany do poczekalni
   (staging area).

3. Wykonujesz polecenie git commit, które bierze pliki z poczekalni i
   zapisuje tę "migawkę" na stałe w katalogu Gita.

**Śledzenie statusu plików**
----------------------------

Najważniejszym poleceniem do sprawdzania, co dzieje się w Twoim
repozytorium, jest git status.

.. code-block:: bash

   $ git status On branch main No commits yet Untracked files: (use "git add ..." to include in what will be committed) plik.txt

Widzimy, że mamy "nieśledzony" (untracked) plik. Oznacza to, że Git
widzi plik, ale nie został on jeszcze dodany do systemu kontroli wersji.

**Zestawienie najważniejszych poleceń**
---------------------------------------

Poniższa tabela podsumowuje komendy niezbędne do rozpoczęcia pracy.

+-----------------------+----------------------------------------------+
| Polecenie             | Opis i zastosowanie                          |
+=======================+==============================================+
| \``git init`\`        | Inicjalizuje nowe, puste repozytorium w      |
|                       | bieżącym katalogu.                           |
+-----------------------+----------------------------------------------+
| \``git clone [url]`\` | Pobiera istniejące repozytorium ze zdalnego  |
|                       | serwera (tworzy lokalną kopię).              |
+-----------------------+----------------------------------------------+
| \``git add [plik]`\`  | Dodaje plik (lub zmiany w pliku) do          |
|                       | poczekalni (staging area).                   |
+-----------------------+----------------------------------------------+
| \``git commit -m      | Zapisuje zmiany z poczekalni jako nową       |
| "[opis]"\`\`          | migawkę (commit) w historii repozytorium.    |
+-----------------------+----------------------------------------------+
| \``git status`\`      | Wyświetla stan katalogu roboczego i          |
|                       | poczekalni (co zmieniono, co jest gotowe).   |
+-----------------------+----------------------------------------------+
| \``git log`\`         | Pokazuje historię zatwierdzeń (commitów) w   |
|                       | repozytorium.                                |
+-----------------------+----------------------------------------------+
