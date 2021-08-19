---
title: Installazione e uso di Input Method Editor
description: Questo articolo offre un'esercitazione su come installare e usare lo standard Windows Input Method Editor (IME).
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45a0da52d0e917186831de8c84f39ecee3d2583ac4a267fa2501c643e2f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153513"
---
# <a name="installing-and-using-input-method-editors"></a>Installazione e uso di Input Method Editor

Questo articolo offre un'esercitazione su come installare e usare lo standard Windows Input Method Editor (IME).

-   [Installazione di input method editor](#installing-an-input-method-editor)
-   [IME cinese semplificato](#simplified-chinese-ime)
-   [IME cinese tradizionale](#traditional-chinese-ime)
-   [IME giapponese](#japanese-ime)
-   [IME coreano](#korean-ime)
-   [Requisiti](#requirements)

## <a name="installing-an-input-method-editor"></a>Installazione di input method editor

Le sezioni seguenti descrivono come installare e usare gli IME (Input Method Editor) per immettere caratteri complessi in quattro diverse lingue dell'Asia orientale. Vengono illustrate le funzionalità specifiche di ogni linguaggio.

Per implementare la funzionalità Input Method Editor (IME) in un'applicazione, vedere [Uso di input method editor in un gioco.](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game)

Un IME non è installato nei sistemi Microsoft Windows XP per impostazione predefinita. Per eseguire l'installazione, seguire questa procedura.

**Per installare un IME**

1.  Dal Pannello di controllo, aprire Opzioni internazionali e della lingua.
2.  Nella scheda Lingue selezionare la casella di controllo Installa file per lingue dell'Asia orientale.

    ![Scheda lingue delle opzioni internazionali e della lingua](images/ime-1.png)

    Verrà visualizzata la finestra di dialogo Installa supporto lingua supplementare che informa i requisiti di archiviazione per i file di lingua.

    ![Finestra di dialogo per l'installazione del supporto linguistico supplementare](images/ime-install-lang-dialog.png)

3.  Fare clic su OK per chiudere la finestra di dialogo.
4.  Fare clic su OK nella scheda Lingue .
5.  Viene visualizzata un'altra finestra di dialogo che richiede Windows disco di installazione di XP o un percorso di condivisione di rete in cui si trovano i file di supporto della lingua. Inserire un Windows disco compatto XP o passare al percorso di rete appropriato e fare clic su OK. Microsoft Windows installa i file necessari e richiede di riavviare il computer.
6.  Fare clic su Sì per riavviare il computer.
7.  Dopo il riavvio, aprire nuovamente il pannello di controllo Opzioni internazionali e della lingua.
8.  Nella scheda Lingue fare clic su Dettagli. Verrà visualizzata la finestra Servizi di testo e lingue di input.

    ![Finestra dei servizi estendi e delle lingue di input](images/ime-2.png)

9.  Nella scheda Impostazioni fare clic su Aggiungi. Verrà visualizzata la finestra Aggiungi lingua di input.

    ![Finestra aggiungi lingua di input](images/ime-3.png)

10. Selezionare Cinese (Taiwan) per lingua di input e Microsoft New Phonetic IME 2002a per layout di tastiera/IME.
11. Fare clic su OK. È ora possibile aggiungere altre lingue e IME in modo simile.
12. Fare di nuovo clic su Aggiungi, selezionare cinese (RPC) per la lingua di input e Cinese (semplificato) - Microsoft Pinyin IME 3.0 per layout di tastiera/IME, quindi fare clic su OK.
13. Fare di nuovo clic su Aggiungi, selezionare giapponese per lingua di input e Microsoft IME Standard 2002 ver. 8.1 per layout di tastiera/IME, quindi fare clic su OK.
14. Fare di nuovo clic su Aggiungi, selezionare Coreano per lingua di input e Sistema di input coreano (IME 2002) per layout di tastiera/IME, quindi fare clic su OK. Nella finestra Servizi di testo e lingue di input la casella di riepilogo Servizi installati dovrebbe ora contenere i quattro IME appena aggiunti.

    ![Casella di riepilogo dei servizi installati](images/ime-7.png)

15. Fare clic su OK per chiudere la finestra Servizi di testo e lingue di input.
16. Fare clic su OK per chiudere il pannello di controllo Opzioni internazionali e della lingua. La Windows barra delle applicazioni dovrebbe ora contenere un indicatore delle impostazioni locali di input cerchiato in rosso. L'esistenza dell'indicatore indica che nel sistema sono state installate più lingue di input.

    ![indicatore che indica che nel sistema sono state installate più lingue di input](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME cinese semplificato

Questa sezione descrive come usare l'IME cinese semplificato (PinYin) con Microsoft Blocco note immettere alcuni caratteri cinesi.

1.  Avviare Blocco note (disponibile dal pulsante Start, quindi selezionare Tutti i programmi e accessori). Digitare alcuni caratteri nella Blocco note. Questi caratteri consentono di visualizzare meglio la finestra IME in un secondo momento.

    ![Screnshot che mostra i caratteri che consentono di visualizzare meglio la finestra I M E in un secondo momento per il cinese semplificato.](images/ime-sc1.png)

2.  Con Blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare Cinese (RPC). La visualizzazione dell'indicatore cambia in CH per riflettere che la nuova lingua di input è il cinese (RPC).

    ![Screenshot che mostra l'indicatore delle impostazioni locali di input per la selezione del cinese (P R C).](images/ime-sc2.png)

3.  Posizionare il cursore nella Blocco note. Premere HOME sulla tastiera in modo che il cursore si trova all'inizio della riga. Sulla tastiera digitare "N", quindi "I". La figura seguente illustra l'aspetto della visualizzazione. Il piccolo rettangolo orizzontale è la finestra di lettura, che visualizza la stringa di lettura corrente. Attualmente, la stringa di lettura è "ni" come risultato della digitazione di "N" e "I".

    ![Screenshot che mostra una stringa di lettura con "n" e "i".](images/ime-sc3.png)

4.  Digitare "3". A Blocco note ora è disponibile la visualizzazione seguente. Poiché N+I+3 è una pronuncia completa in Pinyin in cinese semplificato, l'IME ha informazioni sufficienti per prevedere il carattere che l'utente potrebbe aver previsto di immettere. La finestra di lettura scompare perché è stata immessa una pronuncia completa. Viene visualizzato un carattere sopra il cursore Blocco note corrente. Questo carattere non fa parte di Blocco note, ma viene visualizzato in un'altra finestra sopra Blocco note e nasconde i caratteri esistenti nelle Blocco note sottostanti. Questa nuova finestra è denominata finestra di composizione e la stringa in essa in essa è denominata stringa di composizione. La stringa di composizione è sottolineata nella visualizzazione.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione di un carattere.](images/ime-sc4.png)

5.  Digitare ora "H", "A", "O", "3" per immettere un altro carattere. Si noti che la finestra di lettura viene visualizzata quando viene digitato "H" e scompare quando viene digitato "3". Come illustrato di seguito, la stringa di composizione contiene ora due caratteri.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione di due caratteri.](images/ime-sc5.png)

6.  Premere una volta la freccia sinistra sulla tastiera. Il cursore di composizione sposta un carattere a sinistra, in corrispondenza del secondo carattere digitato. Viene visualizzata una finestra sopra la Blocco note, come illustrato di seguito. Questa finestra è denominata finestra candidata. Visualizza un elenco di caratteri o frasi che corrispondono alla pronuncia digitata. È possibile selezionare la parola prevista dalle voci nell'elenco dei candidati. In questo esempio sono disponibili due caratteri candidati con la stessa pronuncia.

    ![due caratteri candidati disponibili con la stessa pronuncia](images/ime-sc6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata si chiude e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra una stringa di composizione aggiornata con il carattere selezionato.](images/ime-sc7.png)

8.  Premere INVIO. Ciò indica all'IME che la composizione è completa e che la stringa deve essere inviata all'applicazione, Blocco note in questo esempio. La finestra di composizione si chiude e i due caratteri vengono inviati Blocco note tramite WM \_ CHAR. La sottolineatura non è più presente nella figura seguente perché i due caratteri visualizzati fanno parte del testo in Blocco note. Il testo esistente "ABCDEFG" Blocco note viene spostato a destra perché sono stati inseriti altri due caratteri. A questo punto sono stati immessi due caratteri in cinese semplificato usando un IME.

    ![sono stati immessi due caratteri in cinese semplificato usando un ime](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME cinese tradizionale

Questa sezione descrive come usare l'IME per il cinese tradizionale (New Phonetic) con Blocco note per immettere alcuni caratteri cinesi.

1.  Avviare il Blocco note. Digitare alcuni caratteri nella Blocco note. Questi caratteri consentono di visualizzare meglio la finestra IME in un secondo momento.

    ![Screenshot che mostra i caratteri che consentono di visualizzare meglio la finestra I M E in un secondo momento per il cinese tradizionale.](images/ime-tc1.png)

2.  Fare clic sull'indicatore delle impostazioni locali di input Windows barra delle applicazioni e selezionare Cinese (Taiwan). La visualizzazione dell'indicatore cambia in CH per riflettere che la nuova lingua di input è il cinese (Taiwan).

    ![Indicatore delle impostazioni locali di input per selezionare il cinese (Taiwan)](images/ime-tc2.png)

3.  Posizionare il cursore Blocco note. Premere HOME sulla tastiera in modo che il cursore si trova all'inizio della riga. Sulla tastiera digitare "S", quindi "U". La figura seguente illustra l'aspetto della visualizzazione. Il piccolo rettangolo verticale è la finestra di lettura, che visualizza la stringa di lettura corrente. Come illustrato nella figura seguente, la stringa di lettura contiene due caratteri in seguito alla digitazione di "S" e "U".

    ![Screenshot che mostra una stringa di lettura con due caratteri.](images/ime-tc3.png)

4.  Digitare "3". Ora Blocco note visualizzazione seguente. Poiché S+U+3 è una pronuncia completa in cinese tradizionale, l'IME ha informazioni sufficienti per anticipare il carattere che l'utente potrebbe aver previsto di immettere. La finestra di lettura scompare perché è stata immessa una pronuncia completa. Un carattere viene visualizzato sopra il cursore Blocco note testo. Questo carattere non fa parte Blocco note, ma viene visualizzato in un'altra finestra sopra Blocco note e nasconde i caratteri esistenti nelle Blocco note sottostanti. Questa nuova finestra è denominata finestra di composizione e la stringa in essa è denominata stringa di composizione. La stringa di composizione è sottolineata nella visualizzazione.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione sottolineata.](images/ime-tc4.png)

5.  Digitare ora "C", "L" e "3" per immettere un altro carattere. Si noti che la finestra di lettura viene visualizzata quando viene digitato "C" e scompare quando viene digitato "3". Come illustrato di seguito, la stringa di composizione contiene ora due caratteri.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione e due caratteri sottolineati.](images/ime-tc5.png)

6.  Digitare una sola volta la freccia giù sulla tastiera. Viene visualizzata una finestra nella parte superiore Blocco note come illustrato di seguito. Questa finestra è denominata finestra candidata. Visualizza un elenco di caratteri o frasi che corrispondono alla pronuncia digitata. È possibile selezionare la parola prevista dalle voci nell'elenco dei candidati. In questo esempio sono disponibili tre caratteri candidati con la stessa pronuncia.

    ![tre caratteri candidati disponibili con la stessa pronuncia](images/ime-tc6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata si chiude e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra una stringa di composizione aggiornata con un carattere selezionato.](images/ime-tc7.png)

8.  Premere INVIO. Questo indica all'IME che la composizione è completa e che la stringa deve essere inviata all'applicazione, Blocco note in questo esempio. La finestra di composizione viene chiusa e i due caratteri vengono inviati a Blocco note tramite [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). La sottolineatura non è più presente nella figura seguente perché i due caratteri visualizzati fanno parte del testo in Blocco note. Il testo esistente "ABCDEFG" in Blocco note viene spostato a destra perché sono stati inseriti altri due caratteri. A questo punto sono stati immessi due caratteri in cinese tradizionale usando un IME.

    ![sono stati immessi due caratteri in cinese tradizionale usando un ime](images/ime-tc8.png)

## <a name="japanese-ime"></a>IME giapponese

Questa sezione illustra l'uso dell'IME giapponese con Blocco note per immettere alcuni caratteri giapponesi.

1.  Avviare il Blocco note. Digitare alcuni caratteri in Blocco note. Questi caratteri consentono di visualizzare meglio la finestra IME in un secondo momento.

    ![Screenshot che mostra i caratteri che consentono di visualizzare meglio la finestra I M E in un secondo momento per il giapponese.](images/ime-j1.png)

2.  Con Blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare Giapponese. La visualizzazione dell'indicatore cambia in JP per riflettere che la nuova lingua di input è il giapponese.

    ![Indicatore delle impostazioni locali di input per selezionare il giapponese](images/ime-j2.png)

3.  Posizionare il cursore Blocco note. Premere HOME sulla tastiera in modo che il cursore si trova all'inizio della riga. Sulla tastiera digitare "N", quindi "I". La figura seguente illustra l'aspetto della visualizzazione. Poiché N+I è una pronuncia completa in giapponese, l'IME ha informazioni sufficienti per anticipare il carattere che l'utente potrebbe aver previsto di immettere. Un carattere viene visualizzato sopra il cursore Blocco note testo. Questo carattere non fa parte Blocco note, ma viene visualizzato in un'altra finestra sopra Blocco note e nasconde i caratteri esistenti nelle Blocco note sottostanti. Questa nuova finestra è denominata finestra di composizione e la stringa in essa è denominata stringa di composizione. La stringa di composizione è sottolineata nella visualizzazione.

    ![Screenshot che mostra una stringa di composizione con un carattere giapponese sottolineato.](images/ime-j3.png)

4.  Digitare ora "H", "O", "N", "G" e "O" per immettere altri due caratteri. La stringa di composizione contiene ora quattro caratteri, come illustrato di seguito.

    ![Screenshot che mostra una stringa di composizione con quattro caratteri giapponesi sottolineati.](images/ime-j4.png)

5.  Premere la barra spaziatrice. Questo indica all'IME di convertire il testo immesso in clausole. Nella figura seguente l'IME converte la pronuncia "Nihongo" in una clausola scritta in Kanji che significa "lingua giapponese".

    ![ime converte la pronuncia giapponese](images/ime-j5.png)

6.  Premere una volta la freccia giù sulla tastiera. Viene visualizzata una finestra nella parte superiore Blocco note come illustrato di seguito. Questa finestra è denominata finestra candidata. Visualizza un elenco di clausole che corrispondono alla pronuncia digitata. È possibile selezionare la parola prevista dall'elenco di candidati. In questo esempio sono disponibili tre caratteri candidati con la stessa pronuncia. Si noti che la seconda voce è evidenziata e la stringa di composizione cambia. Ciò è causato dalla digitazione della freccia giù, che indica all'IME di selezionare la voce dopo quella visualizzata in precedenza.

    ![Screenshot che mostra la finestra candidata.](images/ime-j6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata si chiude e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra la stringa di composizione aggiornata con il carattere giapponese selezionato.](images/ime-j7.png)

8.  Premere INVIO. Questo indica all'IME che la composizione è completa e che la stringa deve essere inviata all'applicazione, Blocco note in questo esempio. La finestra di composizione viene chiusa e i due caratteri vengono inviati a Blocco note tramite [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). La sottolineatura non è più presente nella figura seguente perché i due caratteri visualizzati fanno parte del testo in Blocco note. Il testo esistente "ABCDEFG" in Blocco note viene spostato a destra perché sono stati inseriti altri due caratteri. A questo punto sono stati immessi alcuni caratteri giapponesi usando un IME.

    ![È stato immesso correttamente alcuni caratteri giapponesi usando un ime](images/ime-j8.png)

## <a name="korean-ime"></a>IME coreano

Questa sezione descrive come usare l'IME coreano con Blocco note per immettere alcuni caratteri coreani.

1.  Avviare il Blocco note. Digitare alcuni caratteri in Blocco note. Questi caratteri consentono di visualizzare meglio la finestra IME in un secondo momento.

    ![caratteri che consentono di visualizzare meglio la finestra ime in un secondo momento](images/ime-k1.png)

2.  Con Blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare Coreano. La visualizzazione dell'indicatore cambia in KO per riflettere che la nuova lingua di input è coreana.

    ![Indicatore delle impostazioni locali di input per selezionare il coreano](images/ime-k2.png)

3.  Posizionare il cursore Blocco note. Premere HOME sulla tastiera in modo che il cursore si trova all'inizio della riga, quindi digitare "G". La figura seguente illustra l'aspetto della visualizzazione. L'elemento fonetico corrispondente a "G" viene visualizzato Blocco note ed è evidenziato con un cursore a blocchi. Questo carattere evidenziato è denominato stringa di composizione. Si noti che a differenza dell'IME per altre lingue, la stringa di composizione viene inviata a Blocco note e inserita a sinistra del testo esistente non appena l'utente immette un singolo elemento fonetico.

    ![Screenshot che mostra una stringa di composizione con un carattere inserito a sinistra del testo esistente.](images/ime-k3.png)

4.  In questo momento, la stringa di composizione è costituita da un carattere provvisorio perché eventuali elementi fonetici aggiuntivi immessi dall'utente modificano la stringa di composizione sul posto. Digitare ora "K", quindi "S". Si noti che il carattere provvisorio cambia a ogni pressione di tasto.

    ![stringa di composizione](images/ime-k4.png)

5.  A questo punto premere il tasto CTRL destro. Viene visualizzata una finestra candidata che elenca i caratteri Hanja che è possibile selezionare per la pronuncia immessa, G+K+S.

    ![Screenshot che mostra una finestra candidata con un elenco di caratteri Hanja che è possibile selezionare nella parte inferiore della finestra.](images/ime-k5.png)

6.  Digitare il numero "1" per selezionare la prima voce nell'elenco. La finestra candidata si chiude e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Stringa di composizione aggiornata con il carattere selezionato](images/ime-k6.png)

7.  Digitare "R", "N" e "R". Premere quindi CTRL a destra per immettere un altro carattere.

    ![finestra candidata](images/ime-k7.png)

8.  Digitare "1" per selezionare la prima voce. A questo punto sono stati immessi due caratteri coreani usando un IME. I caratteri coreani fanno già parte della stringa di testo in Blocco note.

    ![sono stati immessi due caratteri coreani usando un ime](images/ime-k8.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operativo**                | Windows XP                                                                                                 |
| **Spazio disponibile su disco rigido**       | Almeno 230 MB                                                                                            |
| **Percorsi dei file in lingua esterna** | Windows Disco compatto per l'installazione di XP o percorso di rete con Windows file di installazione di XP                |
| **Time**                            | Circa dieci minuti per installare i file di lingua esterna; circa dieci minuti ciascuno per esaminare quattro diversi IME. |



 

 

 
