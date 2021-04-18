---
title: Installazione e utilizzo degli editor del metodo di input
description: Questo articolo fornisce un'esercitazione su come installare e usare l'IME (Input Method Editor) standard di Windows.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6018b3a387a12409f9e46d0392bbd60015af29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324921"
---
# <a name="installing-and-using-input-method-editors"></a>Installazione e utilizzo degli editor del metodo di input

Questo articolo fornisce un'esercitazione su come installare e usare l'IME (Input Method Editor) standard di Windows.

-   [Installazione di un editor del metodo di input](#installing-an-input-method-editor)
-   [IME cinese semplificato](#simplified-chinese-ime)
-   [IME cinese tradizionale](#traditional-chinese-ime)
-   [IME giapponese](#japanese-ime)
-   [IME coreano](#korean-ime)
-   [Requisiti](#requirements)

## <a name="installing-an-input-method-editor"></a>Installazione di un editor del metodo di input

Nelle sezioni seguenti viene descritto come installare e utilizzare input Method Editor (IME) per immettere caratteri complessi in quattro diverse lingue asiatiche orientali. Sono illustrate le funzionalità univoche per ogni lingua.

Per implementare la funzionalità IME (Input Method Editor) in un'applicazione, vedere [utilizzo di un editor del metodo di input in un gioco](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

Per impostazione predefinita, un IME non è installato nei sistemi Microsoft Windows XP. Per installare, completare i passaggi seguenti.

**Per installare un IME**

1.  Nel pannello di controllo aprire Opzioni internazionali e della lingua.
2.  Nella scheda lingue selezionare la casella di controllo Installa i file per le lingue asiatiche orientali.

    ![scheda linguaggi delle opzioni internazionali e della lingua](images/ime-1.png)

    Viene visualizzata una finestra di dialogo per l'installazione del supporto del linguaggio supplementare che informa i requisiti di archiviazione per i file di lingua.

    ![finestra di dialogo per l'installazione del supporto del linguaggio supplementare](images/ime-install-lang-dialog.png)

3.  Fare clic su OK per chiudere la finestra di dialogo.
4.  Fare clic su OK nella scheda lingue.
5.  Viene visualizzata un'altra finestra di dialogo che richiede un disco di installazione di Windows XP o un percorso di condivisione di rete in cui si trovano i file di supporto della lingua Inserire un disco di Windows XP Compact oppure passare al percorso di rete appropriato, quindi fare clic su OK. Microsoft Windows installa i file necessari e richiede il riavvio del computer.
6.  Fare clic su Sì per riavviare il computer.
7.  Dopo il riavvio, aprire nuovamente il pannello di controllo Opzioni internazionali e della lingua.
8.  Nella scheda lingue fare clic su dettagli. Viene visualizzata la finestra servizi di testo e lingue di input.

    ![finestra Servizi EXT e lingue di input](images/ime-2.png)

9.  Nella scheda Impostazioni fare clic su Aggiungi. Viene visualizzata la finestra Aggiungi lingua di input.

    ![finestra Aggiungi lingua di input](images/ime-3.png)

10. Selezionare cinese (Taiwan) per lingua di input e Microsoft New fonetico IME 2002 per layout tastiera/IME.
11. Fare clic su OK. È ora possibile aggiungere altre lingue e IME in modo analogo.
12. Fare di nuovo clic su Aggiungi, selezionare cinese (PRC) per lingua di input e cinese (semplificato)-Microsoft Pinyin IME 3,0 per tastiera layout/IME, quindi fare clic su OK.
13. Fare di nuovo clic su Aggiungi, selezionare giapponese per lingua di input e Microsoft IME Standard 2002 ver. 8,1 per il layout di tastiera/IME, quindi fare clic su OK.
14. Fare di nuovo clic su Aggiungi, selezionare coreano per input language e Korean input System (IME 2002) per layout tastiera/IME, quindi fare clic su OK. Nella finestra servizi di testo e lingue di input la casella di riepilogo servizi installati dovrebbe ora contenere i quattro IME appena aggiunti.

    ![casella di riepilogo servizi installati](images/ime-7.png)

15. Fare clic su OK per chiudere la finestra servizi di testo e lingue di input.
16. Fare clic su OK per chiudere il pannello di controllo Opzioni internazionali e della lingua. La barra delle applicazioni di Windows dovrebbe ora contenere un indicatore delle impostazioni locali di input cerchio in rosso. L'esistenza dell'indicatore indica che nel sistema è stata installata più di una lingua di input.

    ![indicatore che indica che nel sistema è stata installata più di una lingua di input](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME cinese semplificato

In questa sezione viene descritto come utilizzare l'IME cinese semplificato (PinYin) con Microsoft Notepad per immettere alcuni caratteri cinesi.

1.  Avviare il blocco note (disponibile dal pulsante Start, quindi selezionare tutti i programmi e accessori). Digitare alcuni caratteri nel blocco note. Questi caratteri consentiranno di visualizzare più avanti la finestra IME.

    ![Screenshot che mostra i caratteri che consentono di visualizzare la finestra i M E più in seguito per il cinese semplificato.](images/ime-sc1.png)

2.  Con blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare cinese (PRC). L'indicatore Visualizza le modifiche apportate a CH per indicare che la nuova lingua di input è cinese (PRC).

    ![Screenshot che mostra l'indicatore delle impostazioni locali di input per selezionare il cinese (P R C).](images/ime-sc2.png)

3.  Posizionare il cursore nel blocco note. Premere HOME sulla tastiera per fare in modo che il cursore si trovi all'inizio della riga. Sulla tastiera digitare "N", quindi "I". Nella figura seguente viene illustrato l'aspetto della visualizzazione. Il piccolo rettangolo orizzontale è la finestra di lettura, che visualizza la stringa di lettura corrente. Attualmente la stringa di lettura è "NI" in seguito alla digitazione di "N" e "I".

    ![Screenshot che mostra una stringa di lettura con ' n'è i '.](images/ime-sc3.png)

4.  Digitare "3". A questo punto, il blocco note presenta la seguente visualizzazione. Poiché N + I + 3 è una pronuncia completa nel pinyin cinese semplificato, l'IME dispone di informazioni sufficienti per prevedere il carattere che l'utente potrebbe avere intenzione di immettere. La finestra di lettura scompare perché è stata immessa una pronuncia completa. Un carattere viene visualizzato sopra il cursore del blocco note. Questo carattere non fa parte del blocco note, ma viene visualizzato in un'altra finestra nella parte superiore del blocco note e nasconde i caratteri esistenti nel blocco note sotto. Questa nuova finestra è detta finestra di composizione e la stringa in essa rappresenta la stringa di composizione. La stringa di composizione viene sottolineata nella visualizzazione.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione di un carattere.](images/ime-sc4.png)

5.  Digitare ora "H", "A", "O", "3" per immettere un altro carattere. Si noti che la finestra di lettura viene visualizzata quando "H" è tipizzata e scompare quando viene digitato "3". Come illustrato di seguito, la stringa di composizione contiene ora due caratteri.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione di due caratteri.](images/ime-sc5.png)

6.  Premere la freccia sinistra sulla tastiera una volta. Il cursore di composizione sposta un carattere a sinistra, al secondo carattere digitato. Viene visualizzata una finestra nella parte superiore del blocco note, come illustrato di seguito. Questa finestra è detta finestra candidata. Viene visualizzato un elenco di caratteri o frasi che corrispondono alla pronuncia digitata. È possibile selezionare la parola desiderata dalle voci dell'elenco candidato. In questo esempio sono disponibili due caratteri candidati con la stessa pronuncia.

    ![due caratteri candidati disponibili con la stessa pronuncia](images/ime-sc6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata viene ora chiusa e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra una stringa di composizione aggiornata con il carattere selezionato.](images/ime-sc7.png)

8.  Premere INVIO. In questo modo si indica all'IME che la composizione è completata e che la stringa deve essere inviata all'applicazione-blocco note in questo esempio. La finestra di composizione si chiude e i due caratteri vengono inviati al blocco note tramite WM \_ Char. La sottolineatura si trova nella figura seguente perché i due caratteri visualizzati fanno parte del testo del blocco note. Il testo esistente "ABCDEFG" nel blocco note è stato spostato a destra perché sono stati inseriti altri due caratteri. Sono stati immessi correttamente due caratteri in cinese semplificato utilizzando un IME.

    ![immesso correttamente due caratteri in cinese semplificato utilizzando un IME](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME cinese tradizionale

In questa sezione viene descritto come utilizzare l'IME cinese tradizionale (nuovo fonetico) con blocco note per immettere alcuni caratteri cinesi.

1.  Avviare il Blocco note. Digitare alcuni caratteri nel blocco note. Questi caratteri consentiranno di visualizzare più avanti la finestra IME.

    ![Screenshot che mostra i caratteri che consentono di visualizzare la finestra i M E più in seguito per il cinese tradizionale.](images/ime-tc1.png)

2.  Fare clic sull'indicatore delle impostazioni locali di input sulla barra delle applicazioni di Windows e selezionare cinese (Taiwan). L'indicatore Visualizza le modifiche apportate a CH per indicare che la nuova lingua di input è cinese (Taiwan).

    ![indicatore delle impostazioni locali di input per la selezione del cinese (Taiwan)](images/ime-tc2.png)

3.  Posizionare il cursore nel blocco note. Premere HOME sulla tastiera per fare in modo che il cursore si trovi all'inizio della riga. Sulla tastiera digitare "S", quindi "U". Nella figura seguente viene illustrato l'aspetto della visualizzazione. Il rettangolo verticale piccolo è la finestra di lettura, che visualizza la stringa di lettura corrente. Come illustrato nella figura seguente, la stringa di lettura contiene due caratteri in seguito alla digitazione di "S" e "U".

    ![Screenshot che mostra una stringa di lettura con due caratteri.](images/ime-tc3.png)

4.  Digitare "3". A questo punto, il blocco note presenta la seguente visualizzazione. Poiché S + U + 3 è una pronuncia completa nel cinese tradizionale, l'IME dispone di informazioni sufficienti per prevedere il carattere che l'utente potrebbe avere intenzione di immettere. La finestra di lettura scompare perché è stata immessa una pronuncia completa. Un carattere viene visualizzato sopra il cursore del blocco note. Questo carattere non fa parte del blocco note, ma viene visualizzato in un'altra finestra nella parte superiore del blocco note e nasconde i caratteri esistenti nel blocco note sotto. Questa nuova finestra è detta finestra di composizione e la stringa in essa rappresenta la stringa di composizione. La stringa di composizione viene sottolineata nella visualizzazione.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione sottolineata.](images/ime-tc4.png)

5.  Digitare ora "C", "L" e "3" per immettere un altro carattere. Si noti che la finestra di lettura viene visualizzata quando "C" è tipizzata e scompare quando viene digitato "3". Come illustrato di seguito, la stringa di composizione contiene ora due caratteri.

    ![Screenshot che mostra una finestra di composizione con una stringa di composizione e due caratteri sottolineati.](images/ime-tc5.png)

6.  Digitare la freccia giù sulla tastiera una volta. Viene visualizzata una finestra nella parte superiore del blocco note, come illustrato di seguito. Questa finestra è detta finestra candidata. Viene visualizzato un elenco di caratteri o frasi che corrispondono alla pronuncia digitata. È possibile selezionare la parola desiderata dalle voci dell'elenco candidato. In questo esempio sono disponibili tre caratteri candidati con la stessa pronuncia.

    ![tre caratteri candidati disponibili con la stessa pronuncia](images/ime-tc6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata viene ora chiusa e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra una stringa di composizione aggiornata con un carattere selezionato.](images/ime-tc7.png)

8.  Premere INVIO. In questo modo si indica all'IME che la composizione è completata e che la stringa deve essere inviata all'applicazione-blocco note in questo esempio. La finestra di composizione si chiude e i due caratteri vengono inviati al blocco note tramite [**WM \_ char**](/windows/desktop/inputdev/wm-char). La sottolineatura si trova nella figura seguente perché i due caratteri visualizzati fanno parte del testo del blocco note. Il testo esistente "ABCDEFG" nel blocco note è stato spostato a destra perché sono stati inseriti altri due caratteri. Sono stati immessi correttamente due caratteri cinesi tradizionali utilizzando un IME.

    ![immesso correttamente due caratteri cinesi tradizionali utilizzando un IME](images/ime-tc8.png)

## <a name="japanese-ime"></a>IME giapponese

Questa sezione descrive come usare l'IME giapponese con blocco note per immettere alcuni caratteri giapponesi.

1.  Avviare il Blocco note. Digitare alcuni caratteri nel blocco note. Questi caratteri consentiranno di visualizzare più avanti la finestra IME.

    ![Screenshot che mostra i caratteri che consentono di visualizzare la finestra i M E più in seguito per il giapponese.](images/ime-j1.png)

2.  Con blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare giapponese. L'indicatore Visualizza le modifiche apportate a JP per indicare che la nuova lingua di input è giapponese.

    ![indicatore delle impostazioni locali di input per selezionare il giapponese](images/ime-j2.png)

3.  Posizionare il cursore nel blocco note. Premere HOME sulla tastiera per fare in modo che il cursore si trovi all'inizio della riga. Sulla tastiera digitare "N", quindi "I". Nella figura seguente viene illustrato l'aspetto della visualizzazione. Poiché N + I è una pronuncia completa in giapponese, l'IME dispone di informazioni sufficienti per prevedere il carattere che l'utente potrebbe avere intenzione di immettere. Un carattere viene visualizzato sopra il cursore del blocco note. Questo carattere non fa parte del blocco note, ma viene visualizzato in un'altra finestra nella parte superiore del blocco note e nasconde i caratteri esistenti nel blocco note sotto. Questa nuova finestra è detta finestra di composizione e la stringa in essa rappresenta la stringa di composizione. La stringa di composizione viene sottolineata nella visualizzazione.

    ![Screenshot che mostra una stringa di composizione con un carattere giapponese sottolineato.](images/ime-j3.png)

4.  Digitare ora "H", "O", "N", "G" e "O" per immettere altri due caratteri. La stringa di composizione ora contiene quattro caratteri, come illustrato di seguito.

    ![Screenshot che mostra una stringa di composizione con quattro caratteri giapponesi sottolineati.](images/ime-j4.png)

5.  Premere la barra spaziatrice. In questo modo si indica all'IME di convertire il testo immesso in clausole. Nella figura seguente l'IME converte la pronuncia "Nihongo" in una clausola scritta in kanji che significa "lingua giapponese".

    ![IME converte la pronuncia giapponese](images/ime-j5.png)

6.  Premere la freccia giù sulla tastiera una volta. Viene visualizzata una finestra nella parte superiore del blocco note, come illustrato di seguito. Questa finestra è detta finestra candidata. Viene visualizzato un elenco di clausole che corrispondono alla pronuncia digitata. È possibile selezionare la parola desiderata dall'elenco di candidati. In questo esempio sono disponibili tre caratteri candidati con la stessa pronuncia. Si noti che la seconda voce è evidenziata e la stringa di composizione viene modificata. Questa operazione è causata dalla digitazione della freccia verso il basso, che indica all'IME di selezionare la voce dopo quella visualizzata in precedenza.

    ![Screenshot che mostra la finestra candidata.](images/ime-j6.png)

7.  Digitare "2" per selezionare la seconda voce. La finestra candidata viene ora chiusa e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![Screenshot che mostra la stringa di composizione aggiornata con il carattere giapponese selezionato.](images/ime-j7.png)

8.  Premere INVIO. In questo modo si indica all'IME che la composizione è completata e che la stringa deve essere inviata all'applicazione-blocco note in questo esempio. La finestra di composizione si chiude e i due caratteri vengono inviati al blocco note tramite [**WM \_ char**](/windows/desktop/inputdev/wm-char). La sottolineatura si trova nella figura seguente perché i due caratteri visualizzati fanno parte del testo del blocco note. Il testo esistente "ABCDEFG" nel blocco note è stato spostato a destra perché sono stati inseriti altri due caratteri. Sono stati immessi correttamente alcuni caratteri giapponesi utilizzando un IME.

    ![sono stati immessi alcuni caratteri giapponesi utilizzando un IME](images/ime-j8.png)

## <a name="korean-ime"></a>IME coreano

In questa sezione viene descritto come utilizzare l'IME coreano con blocco note per immettere alcuni caratteri coreani.

1.  Avviare il Blocco note. Digitare alcuni caratteri nel blocco note. Questi caratteri consentiranno di visualizzare più avanti la finestra IME.

    ![caratteri che consentono di visualizzare la finestra IME in modo più efficace in un secondo momento](images/ime-k1.png)

2.  Con blocco note come applicazione attiva, fare clic sull'indicatore delle impostazioni locali di input e selezionare coreano. L'indicatore Visualizza le modifiche apportate a KO per indicare che la nuova lingua di input è il coreano.

    ![indicatore delle impostazioni locali di input per selezionare il coreano](images/ime-k2.png)

3.  Posizionare il cursore nel blocco note. Premere HOME sulla tastiera per fare in modo che il cursore si trovi all'inizio della riga, quindi digitare "G". Nella figura seguente viene illustrato l'aspetto della visualizzazione. L'elemento fonetico corrispondente a "G" viene visualizzato nel blocco note ed è evidenziato con un cursore a blocchi. Questo carattere evidenziato è denominato stringa di composizione. Si noti che, a differenza dell'IME per altri linguaggi, la stringa di composizione viene inviata al blocco note e inserita a sinistra del testo esistente non appena l'utente immette un singolo elemento fonetico.

    ![Screenshot che mostra una stringa di composizione con un carattere inserito a sinistra del testo esistente.](images/ime-k3.png)

4.  A questo punto, la stringa di composizione è costituita da un carattere provvisorio perché qualsiasi elemento fonetico aggiuntivo immesso dall'utente modifica la stringa di composizione sul posto. Digitare ora "K" e quindi "S". Si noti che il carattere provvisorio cambia con ogni sequenza di tasti.

    ![stringa di composizione](images/ime-k4.png)

5.  A questo punto premere il tasto CTRL. Viene visualizzata una finestra candidata in cui sono elencati i caratteri Hanja che è possibile selezionare per la pronuncia immessa, G + K + S.

    ![Screenshot che mostra una finestra candidata con un elenco di caratteri Hanja che è possibile selezionare nella parte inferiore della finestra.](images/ime-k5.png)

6.  Digitare il numero "1" per selezionare la prima voce nell'elenco. La finestra candidata si chiude e la stringa di composizione viene aggiornata con il carattere selezionato.

    ![stringa di composizione aggiornata con il carattere selezionato](images/ime-k6.png)

7.  Digitare "R", "N" e "R". Premere quindi il tasto CTRL a destra per immettere un altro carattere.

    ![finestra candidata](images/ime-k7.png)

8.  Digitare "1" per selezionare la prima voce. Sono stati immessi correttamente due caratteri coreani utilizzando un IME. I caratteri coreani fanno già parte della stringa di testo nel blocco note.

    ![immesso correttamente due caratteri coreani utilizzando un IME](images/ime-k8.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operativo**                | Windows XP                                                                                                 |
| **Spazio disponibile su disco rigido**       | Almeno 230 MB                                                                                            |
| **Percorsi di file in lingua straniera** | Installazione di Windows XP Compact disk o percorso di rete con i file di installazione di Windows XP                |
| **Time**                            | Circa dieci minuti per installare i file in lingua straniera; circa dieci minuti per esaminare quattro diversi IME. |



 

 

 
