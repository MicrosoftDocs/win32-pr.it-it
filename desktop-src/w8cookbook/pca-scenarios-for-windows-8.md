---
title: Scenari di compatibilità dei programmi per Windows 8
description: Scenari di compatibilità dei programmi per Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebada2ca5115d24f260808a1c9ae899963184a8
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104568820"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Scenari di compatibilità dei programmi per Windows 8

## <a name="platforms"></a>Piattaforme

**Client** -Windows XP Windows \| Vista Windows 7 Windows \| \| 8  

## <a name="description"></a>Descrizione

Program Compatibility Assistant (PCA) è una funzionalità di Windows 8 che consente agli utenti finali di eseguire applicazioni desktop progettate per versioni precedenti di Windows. Windows 8 offre una straordinaria compatibilità tra app che consente alle app progettate per Windows 7 o versioni precedenti di Windows di funzionare in modo automatico in Windows 8. Tuttavia, esiste un numero ridotto di app che possono avere problemi di esecuzione senza intervento.

Quando un utente esegue un'app, PCA tiene traccia dell'app e identifica i sintomi di determinati problemi di compatibilità noti in Windows 8. Quando rileva i sintomi del problema, offre all'utente la possibilità di applicare una correzione consigliata che consentirà di eseguire l'app in modo più efficace in Windows 8.

## <a name="scenarios"></a>Scenari

PCA tiene traccia delle app per una serie di problemi di compatibilità noti in Windows 8. PCA tiene traccia dei problemi, identifica le correzioni e fornisce una finestra di dialogo all'utente con istruzioni per l'applicazione di una correzione consigliata. L'utente può decidere di applicare le correzioni consigliate oppure scegliere di non eseguire alcuna operazione e annullare le indicazioni. Se l'utente annulla l'operazione, l'app non sarà più tenuta in PCA.

PCA in genere applica una delle tre modalità di compatibilità di Windows: Windows XP SP3, Windows Vista SP2 o Windows 7, a seconda del momento in cui è stato creato il programma (o la relativa impostazione). PCA utilizza gli \_ attributi di versione di data e sottosistema del programma e le sezioni di compatibilità e TRUSTINFO del manifesto del file eseguibile per determinare quale delle modalità è pertinente e applica Windows XP SP3 (include i privilegi amministrativi), Windows Vista SP2 o Windows 7 rispettivamente. Un glossario alla fine del documento elenca ogni modalità di compatibilità applicata da PCA e la relativa descrizione.

Per tutti gli scenari elencati di seguito, PCA tiene traccia delle app per una seconda volta dopo l'applicazione di una correzione. Se l'app continua a non riuscire nello stesso modo anche dopo l'applicazione di una correzione della compatibilità, la correzione verrà ripristinata. PCA arresterà definitivamente il monitoraggio dell'app specifica non riuscita.

Sebbene PCA rilevi molti potenziali problemi, non tutti i problemi provocheranno effettivamente errori dell'app. PCA consiglia correzioni solo in situazioni in cui c'è una probabilità elevata che l'errore dell'app è dovuto a motivi di compatibilità di Windows. Le sezioni seguenti si espandono su ognuno degli scenari PCA sviluppati in Windows 8. Ogni sezione descrive lo scenario problematico e le raccomandazioni fornite da PCA per consentire all'app di continuare a funzionare correttamente in Windows 8.

Per ulteriori informazioni sulle modifiche di compatibilità in Windows 8, consultare gli altri argomenti della Guida di riferimento per la *compatibilità con Windows 8*.

Gli scenari in cui PCA rileva e consiglia le correzioni sono:

-   L'installazione o la disinstallazione dell'app non riesce
-   Non è possibile eseguire l'app con un messaggio di controllo della versione di Windows
-   Non è possibile avviare l'app a causa di privilegi amministrativi
-   Arresti anomali dell'app a causa di problemi di memoria specifici
-   L'app ha esito negativo a causa di file di sistema non corrispondenti
-   L'app ha esito negativo a causa di errori non gestiti in Windows a 64 bit
-   L'app non riesce durante il tentativo di eliminare i file non Windows protetti
-   L'app non riesce durante il tentativo di modificare i file di Windows
-   L'app non riesce a causa dell'uso di modalità colori a 8 o 16 bit
-   L'app non riesce a causa di problemi di visualizzazione e grafica
-   L'app non riesce a dichiarare la consapevolezza DPI
-   L'app non riesce perché mancano le funzionalità di Windows
-   L'app non riesce a causa di driver non firmati su Windows 8 a 64 bit
-   Rilevamento delle app installate tramite le impostazioni di compatibilità
-   L'app non è in grado di avviare i programmi di installazione o gli aggiornamenti
-   Programmi di installazione di app che devono essere eseguiti con privilegi amministrativi
-   Applet del pannello di controllo legacy che devono essere eseguiti con privilegi amministrativi

Ognuno di questi scenari è espanso di seguito:

**L'installazione o la disinstallazione dell'app non riesce**

Uno dei tipi più comuni di errori dell'app si verifica durante l'installazione dell'app. I programmi di installazione precedenti hanno in genere esito negativo in due modi:

-   Il programma di installazione non è in grado di riconoscere le funzionalità di controllo dell'account utente in Windows 8, pertanto potrebbe non essere eseguito con i privilegi completi necessari per apportare modifiche al sistema nelle aree protette di Windows 8
-   Il programma di installazione verifica la versione di Windows e blocca l'esecuzione se la versione è superiore a quella prevista

Queste condizioni di errore sono due dei tipi più comuni di errori di compatibilità nel programma di installazione. PCA, con l'ausilio di diversi altri componenti di Windows, ad esempio UAC, rileva i programmi di installazione all'avvio e li tiene traccia fino alla fine dell'installazione. Se il programma di installazione non è in grado di aggiungere i file o di aggiungere una voce valida nella parte ' Aggiungi Rimuovi programmi ' del pannello di controllo di Windows, l'installazione di PCA considera non riuscita.

In questo caso, PCA consiglia una modalità di compatibilità appropriata per l'app. La modalità di compatibilità consente l'esecuzione del programma di installazione in modalità Windows per cui è stato progettato e garantisce inoltre che l'app venga eseguita con privilegi amministrativi. PCA applica la modalità di compatibilità RUNASADMIN con la modalità di compatibilità di Windows XP, Windows Vista o Windows 7 appropriata. L'utente, al termine dell'installazione non riuscita, visualizzerà una finestra di dialogo con la raccomandazione PCA:

![finestra di dialogo di installazione o disinstallazione dell'app non riuscita](images/pcafigure1.png)

L'utente può quindi scegliere di:

-   Eseguire il programma usando le impostazioni di compatibilità (opzione consigliata), dopo le quali PCA applicherà l'impostazione consigliata (modalità compatibilità), riavvierà il programma di installazione e lo rileverà fino a quando l'installazione non verrà completata correttamente.
-   Indica che il programma è installato correttamente, nel qual caso PCA non aggiungerà alcuna impostazione e arresterà il monitoraggio dell'installazione
-   Fare clic su Chiudi. in questo caso PCA non aggiungerà alcuna impostazione e arresterà il monitoraggio dell'installazione

Lo stesso meccanismo viene usato per facilitare la disinstallazione dell'app quando un utente tenta di disinstallare l'app dalla sezione ' installazione applicazioni ' in Windows o dal collegamento di disinstallazione dell'app.

**Non è possibile eseguire l'app con un messaggio di controllo della versione di Windows**

Uno degli errori di compatibilità più comuni nel runtime dell'app è dovuto al controllo della versione di Windows. Molte app, al momento dell'avvio, verifica la versione di Windows; Se non riconoscono la versione, si bloccano anche se l'app potrebbe essere stata eseguita senza problemi.

In genere, tali controlli sono associati a due condizioni che la PCA tiene traccia:

L'app visualizza una finestra di messaggio che avvisa l'utente. Di seguito è riportato un esempio:

![non è possibile eseguire l'app con una finestra di dialogo di controllo della versione di Windows](images/pcafigure2.png)

-   L'app termina immediatamente o si arresta in modo anomalo

Se PCA identifica entrambe le condizioni per un'app, fornirà una raccomandazione all'utente. PCA consentirà all'utente di eseguire di nuovo l'app con le impostazioni di compatibilità. PCA applicherà la modalità di compatibilità di Windows XP, Windows Vista o Windows 7 appropriata basata sull'app. Come in uno degli scenari, l'utente può indicare a PCA che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante Chiudi. Di seguito è riportata una finestra di dialogo di esempio:

![non è possibile eseguire l'app con una finestra di dialogo di opzioni del messaggio di controllo della versione](images/pcafigure3.png)

**Non è possibile avviare o eseguire l'app a causa di privilegi amministrativi**

Alcune app richiedono privilegi amministrativi per l'esecuzione e l'esecuzione delle relative funzionalità. Tuttavia, in Windows 8, analogamente a Windows 7 e Windows Vista, le app vengono eseguite in livelli di privilegi inferiori per impostazione predefinita a causa del controllo dell'account utente. Le app più recenti progettate per Windows Vista e versioni successive dichiarano in genere il livello di privilegio che devono essere eseguite in utilizzando la sezione TRUSTINFO del manifesto EXE. Tuttavia, le app meno recenti in genere hanno esito negativo in due modi:

-   App Visualizza un messaggio all'utente che richiede privilegi amministrativi, come nell'esempio seguente:

![Impossibile avviare o eseguire l'app a causa di una finestra di dialogo con privilegi amministrativi](images/pcafigure4a.png)

-   L'app termina immediatamente o si arresta in modo anomalo

Se PCA identifica entrambe le condizioni per un'app, fornirà una raccomandazione all'utente. PCA consentirà all'utente di eseguire di nuovo l'app con privilegi amministrativi (la modalità di compatibilità RUNASHIGHEST viene applicata da PCA). L'utente riceverà una richiesta di controllo dell'account utente quando l'app viene riavviata. Come in uno degli scenari, l'utente può scegliere di eseguire nuovamente con l'impostazione consigliata o rifiutare esplicitamente le impostazioni consigliate facendo clic su Chiudi. Di seguito è riportata una finestra di dialogo di esempio:

![Impossibile avviare o eseguire l'app a causa della finestra di dialogo Opzioni privilegi amministrativi](images/pcafigure5.png)

**Arresti anomali dell'app a causa di problemi di memoria specifici**

Alcune app si arrestano in modo anomalo a causa di un problema noto di memoria. L'app fa riferimento a una DLL dalla memoria e quindi chiama una funzione per eseguire il codice nella stessa DLL. Questo causa un arresto anomalo immediato dell'app. Sebbene il problema non sia dovuto alle modifiche di compatibilità di Windows 8, si tratta di un problema relativamente comune riscontrato in un'ampia gamma di app. PCA tiene traccia di questo problema per offrire agli utenti la possibilità di eseguire l'app in modo più affidabile.

Per queste app, PCA applica automaticamente la modalità di compatibilità PINDLL in modo invisibile all'utente. La modalità di compatibilità richiamata da PCA impedisce all'app di liberare la DLL dalla memoria. Quindi, la chiamata di funzione nella DLL da parte dell'app funzionerà, impedendo l'arresto anomalo dell'app e consentendo di continuare a funzionare correttamente.

**L'app ha esito negativo a causa di file di sistema non corrispondenti**

Alcune app progettate per Windows XP e versioni precedenti includono copie delle DLL di sistema di Windows insieme ai relativi programmi di installazione. Quando si installano queste app, l'app ha una copia precedente della DLL nella propria cartella, nonché la versione più recente della DLL presente nelle cartelle di sistema di Windows.

In Windows Vista e versioni successive questa condizione può causare un errore dell'app quando tenta di caricare la DLL locale, perché questa DLL non funzionerà correttamente con il resto delle DLL di sistema di Windows correnti. Poiché l'app non è in genere in grado di riconoscere le versioni più recenti di questa DLL, non funziona correttamente.

Quando PCA rileva che la DLL non è stata caricata correttamente, verrà applicata un'impostazione di compatibilità che consente a Windows di caricare la versione più recente della DLL dalla cartella di sistema di Windows in modo che l'app possa essere eseguita correttamente.

Al termine della prima esecuzione non riuscita dell'app, gli utenti visualizzeranno la finestra di dialogo PCA che notifica l'impostazione applicata come indicato di seguito:

![l'app non riesce a causa di una finestra di dialogo file di sistema non corrispondente](images/pcafigure6.png)

**L'app ha esito negativo a causa di errori non gestiti in Windows a 64 bit**

Nella versione a 64 bit di Windows 8 è stata abilitata una nuova eccezione per il meccanismo di callback del ciclo di messaggi. Mentre questa eccezione è stata introdotta per la prima volta in Windows 7, non è obbligatorio gestire questo errore. In Windows 8, le app che usano i cicli di messaggi devono gestire questa nuova eccezione. In caso contrario, si arresteranno in modo anomalo. Le app progettate per versioni precedenti di Windows potrebbero non essere a conoscenza di questa eccezione e quindi potrebbero non gestire correttamente questo errore (eccezione).

PCA rileva le app che non riescono a causa di questo errore non gestito e applica automaticamente la modalità di compatibilità DISABLEUSERCALLBACKEXCEPTION per l'app. Quando l'impostazione viene applicata alla fine dell'esecuzione, l'utente riceve una notifica come indicato di seguito. L'app otterrà la modalità alla successiva esecuzione e sarà in grado di evitare questo errore.

![l'app ha esito negativo a causa di errori non gestiti nella finestra di dialogo Windows a 64 bit](images/pcafigure7.png)

**L'app non riesce durante il tentativo di eliminare i file non Windows protetti**

Alcune app progettate per Windows XP e precedenti presuppongono che in genere siano eseguite con privilegi amministrativi completi. Come un normale comportamento dell'app, possono tentare di eliminare i file non Windows protetti (nei file di programma o nelle cartelle di Windows). Quando l'operazione di eliminazione ha esito negativo, molte di queste app possono arrestarsi.

PCA rileva le app che non riescono a eliminare i file protetti e arrestano l'arresto anomalo e fornisce un'indicazione all'utente. PCA consentirà all'utente di eseguire di nuovo l'app con le impostazioni di compatibilità. Come in uno degli scenari, l'utente può indicare a PCA che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante Chiudi. In questo caso PCA applica la modalità di compatibilità VIRTUALIZEDELETE. Di seguito è riportata una finestra di dialogo di esempio:

![l'app non riesce durante il tentativo di eliminare la finestra di dialogo file protetti non Windows](images/pcafigure8.png)

**Errore dell'app durante il tentativo di modificare i file di Windows o le chiavi del registro di sistema**

Alcune app progettate per Windows XP e precedenti presuppongono che in genere siano eseguite con privilegi amministrativi completi. Come un normale comportamento dell'app, può tentare di modificare, eliminare o scrivere file protetti da Windows (in file di programma o cartelle di Windows) o chiavi del registro di sistema di proprietà di Windows. Quando una delle operazioni di scrittura, eliminazione o modifica di un file o di una chiave del registro di sistema ha esito negativo, molte app potrebbero arrestarsi in modo anomalo o non funzionare

PCA rileva le app che non riescono a scrivere nei file Windows protetti o nelle chiavi del registro di sistema e fornisce un'indicazione all'utente quando l'app si chiude. PCA consentirà all'utente di eseguire di nuovo l'app con le impostazioni di compatibilità. Come in uno degli scenari, l'utente può indicare a PCA che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante Chiudi. In questo caso PCA applica la modalità di compatibilità WRPMITIGATION. Di seguito è riportata una finestra di dialogo di esempio:

![errore dell'app durante il tentativo di modificare la finestra di dialogo file di Windows o chiavi del registro di sistema](images/pcafigure9.png)

**L'app non riesce a causa dell'uso di modalità colori a 8 o 16 bit**

Come parte della rivisitazione di Windows 8 per le app di Windows Store, una delle principali modifiche è che il Gestione finestre desktop (DWM) supporterà solo i colori a 32 bit in Windows 8. Sono ora simulate le modalità a colori inferiori.

Molte app e giochi meno recenti progettati per Windows XP o prima usano le modalità a colori a 8 bit o a 16 bit. Senza mitigazione, queste app potrebbero non essere eseguite in Windows 8. Tuttavia, quando queste app enumerano o tentano di usare una delle modalità colori a 8 o 16 bit per la visualizzazione, PCA identifica immediatamente il problema e, con l'aiuto di DWM, garantisce che l'app funzioni correttamente con la modalità colori simulata.

Si noti che questo problema si verifica non appena l'app richiede le modalità di colore basso ed è trasparente per l'utente. L'utente non deve riavviare l'app per ottenere questa attenuazione perché questa correzione è sempre necessaria per verificare che l'app funzioni correttamente.

**Errore dell'applicazione a causa di problemi di visualizzazione e grafica**

Poiché Gestione finestre desktop (DWM) è sempre attiva in Windows 8, alcune app precedenti di Windows XP possono avere esito negativo se l'app usa API grafiche in modalità mista, come nell'uso delle API GDI e DirectX per il richiamo sullo schermo (soprattutto Giochi meno recenti) e prova a usare la modalità schermo intero:

-   DWM impedisce il disegno direttamente sul desktop e il gioco o l'app avranno esito negativo oppure disegnare una schermata nera sul desktop e non sarà visibile alcuna immagine
-   In questi casi, quando l'app viene chiusa, Windows rileva che l'app o il gioco presenta un problema con la modalità schermo intero e applica la modalità di compatibilità DXMAXIMIZEDWINDOWEDMODE che consente l'esecuzione dell'app o del gioco in una modalità a finestra ingrandita anziché in modalità schermo intero.
-   Dopo che l'impostazione è stata applicata alla fine dell'esecuzione, l'utente riceve una notifica da PCA come illustrato di seguito. l'app otterrà la modalità di compatibilità alla successiva esecuzione e sarà in grado di funzionare correttamente.

![errore dell'applicazione a causa della finestra di dialogo problemi di visualizzazione e grafica](images/pcafigure10.png)

**L'app non riesce a dichiarare la consapevolezza DPI**

Un altro problema tipico di visualizzazione con molte app meno recenti si verifica quando Windows e l'app vengono eseguiti in modalità a DPI elevato, ma l'app non dichiara la consapevolezza del valore DPI elevato tramite il manifesto EXE. Tra i problemi comuni che possono verificarsi a causa di questa mancata corrispondenza nelle impostazioni sono gli elementi dell'interfaccia utente ritagliati o il testo e le dimensioni del carattere non corrette. Per ulteriori informazioni sui problemi, vedere [questo collegamento.](/previous-versions//dd464660(v=vs.85))

In questi casi, Windows rileva che l'app è compatibile con DPI elevato e applica la modalità di compatibilità HIGHDPIAWARE all'app al termine della prima esecuzione. PCA informa quindi l'utente in merito a quanto illustrato di seguito:

![Impossibile dichiarare la finestra di dialogo di riconoscimento dpi dell'app](images/pcafigure11.png)

**Errore dell'applicazione a causa di funzionalità di Windows mancanti**

Alcune app dipendono dalle funzionalità di Windows che sono state rimosse da Windows Vista. Quando queste app tentano di caricare le dll o i componenti COM mancanti, non riescono a funzionare.

PCA rileva le app quando prova a caricare le funzionalità di Windows mancanti e fornisce un suggerimento per scaricare questi componenti e installarli al termine dell'applicazione. L'utente può fare clic su "Get Help online" per trovare un'alternativa o per scaricare la funzionalità e installarla. Se necessario, l'utente può scegliere di non eseguire alcuna operazione facendo clic su Chiudi.

![errore dell'applicazione a causa della finestra di dialogo funzionalità Windows mancante](images/pcafigure12.png)

**L'app non riesce a causa di driver non firmati su Windows 8 a 64 bit**

i driver con firma digitale (file SYS) di Windows a 64 bit sono necessari a partire da Windows Vista. Tuttavia, le app precedenti sono state progettate prima del rilascio di driver forniti da Windows Vista senza firma digitale. Se è installato un driver non firmato di questo tipo, Windows non li caricherà. In rari casi, è possibile che Windows non venga avviato se tali driver sono contrassegnati come driver della fase di avvio.

Alcune app precedenti installano driver non firmati in Windows a 64 bit. Qualsiasi dispositivo o app che tenti di usare questo driver potrebbe non riuscire o causare un arresto anomalo del sistema. Per evitare questo scenario, PCA rileva le app durante l'installazione di driver non firmati e Disabilita il driver perché è contrassegnato come driver della fase di avvio.

Indica inoltre all'utente di acquisire un driver con firma digitale affinché l'app funzioni correttamente. Il messaggio viene visualizzato in seguito all'installazione del driver e in seguito all'installazione dell'app. Se un'altra app installa lo stesso driver, l'app otterrà anche lo stesso messaggio.

![l'app non riesce a causa di driver non firmati nella finestra di dialogo di Windows 8 a 64 bit](images/pcafigure13.png)

**Rilevamento delle app installate tramite le impostazioni di compatibilità**

Quando un programma di installazione ha esito negativo, PCA aiuta il programma di installazione con varie modalità di compatibilità a seconda del tipo di errore. Quando il programma di installazione ha esito positivo con le impostazioni di compatibilità, PCA tiene traccia dei collegamenti aggiunti dal programma di installazione. Questa operazione viene eseguita per verificare se per le app installate potrebbero essere necessarie anche le impostazioni di compatibilità applicate al programma di installazione.

Quando un utente avvia tale app, PCA chiede all'utente di chiedere se l'app funzionava correttamente. Se l'utente risponde, "Sì", la PCA interrompe il rilevamento dell'app. Se l'utente risponde a "No", applica la stessa modalità di compatibilità applicata al programma di installazione dell'app ed esegue di nuovo l'app con la modalità di compatibilità applicata.

**L'app non è in grado di avviare i programmi di installazione o gli aggiornamenti**

Le app a volte avviano programmi figlio che devono essere eseguiti come amministratori. Si tratta in genere del caso in cui un'app tenta di avviare il software di aggiornamento per controllare e installare i nuovi aggiornamenti nell'app. Quando le app eseguono direttamente tali programmi figlio, l'avvio del programma figlio potrebbe non riuscire perché l'app non ha privilegi amministrativi o perché il programma figlio non è stato contrassegnato correttamente per l'elevazione dei privilegi con il manifesto UAC.

PCA tiene traccia di questi errori e quando l'app primaria si chiude, applica automaticamente la modalità di compatibilità ELEVATECREATEPROCESS che consente di eseguire correttamente i programmi figlio. Quando l'app avvia l'app figlio nelle esecuzioni successive, l'utente visualizzerà una finestra di dialogo del controllo dell'account utente per il programma figlio.

Un esempio della finestra di dialogo PCA è illustrato di seguito:

![l'app non è in grado di avviare la finestra di dialogo programmi di installazione o aggiornamento](images/pcafigure14.png)

**Programmi di installazione di app che devono essere eseguiti con privilegi amministrativi**

I programmi di installazione delle app desktop di Windows richiedono privilegi amministrativi perché scrivono file, cartelle e voci del registro di sistema nelle aree di sistema protette. Windows (UAC) dispone di logica di rilevamento per identificare quando viene eseguito un programma di installazione e richiede immediatamente all'utente di fornire privilegi amministrativi tramite la finestra di dialogo controllo dell'account utente. Tuttavia, in alcuni casi, questa logica non sarà in grado di determinare che un'app è effettivamente un programma di installazione e potrebbe non ottenere privilegi amministrativi. Si tratta in genere di programmi di installazione personalizzati che non usano tecnologie di installazione ben note, ad esempio Windows Installer o Install Shield.

In questi casi, la PCA rileva che il programma di installazione non è riuscito a scrivere i propri file. Al termine dell'installazione, PCA fornirà una raccomandazione per applicare le impostazioni di compatibilità. Se l'utente sceglie di fare clic su' Esegui programma ', PCA applicherà la modalità di compatibilità RUNASADMIN ed eseguirà di nuovo il programma di installazione. Se l'utente sceglie di chiudere, non verrà applicata alcuna impostazione. Di seguito è riportato un esempio di finestra di dialogo PCA:

![Screenshot che mostra un esempio di finestra di dialogo per un programma di installazione di app che deve essere eseguito con privilegi amministrativi.](images/pcafigure15.png)

Le applet del pannello di controllo legacy che devono essere eseguite con il pannello di controllo dei privilegi amministrativi vengono in genere modificate dalle impostazioni di sistema e richiedono la possibilità di eseguire l'amministratore di ad. Tuttavia, quelli scritti prima di Windows Vista non dispongono di un manifesto EXE o non hanno la sezione TRUSTINFO che dichiara il livello di privilegio necessario. Quando tali applet vengono eseguiti, PCA li rileva e, al termine della prima esecuzione, fornisce un Consiglio per l'esecuzione con le impostazioni amministrative. Se l'utente sceglie di fare clic su' Esegui programma ', PCA applica la modalità di compatibilità RUNASADMIN ed esegue di nuovo il programma di installazione. Se l'utente sceglie di chiudere, non verrà applicata alcuna impostazione. Di seguito è riportato un esempio di finestra di dialogo PCA:

![programmi di installazione app che devono essere eseguiti con la finestra di dialogo dei privilegi amministrativi](images/pcafigure16.png)

**Verifica delle impostazioni consigliate tramite commenti e suggerimenti degli utenti**

Alla fine di ognuno degli scenari (dopo l'esecuzione dell'app con le impostazioni di compatibilità consigliate), PCA chiederà all'utente una semplice domanda:

![Verifica delle impostazioni consigliate tramite la finestra di dialogo Commenti e suggerimenti degli utenti](images/pcafigure17.png)

L'utente può fornire commenti e suggerimenti se l'app ha funzionato o meno con l'impostazione di compatibilità. Questi dati verranno inviati in modo anonimo a Microsoft. Ciò consente di garantire che tali correzioni possano essere integrate in Windows 8 tramite il processo di aggiornamento di Windows, in modo che gli utenti futuri di Windows 8 non riscontrino più l'errore dell'app e che la PCA non debba più tenere traccia dell'errore nell'app.

**Rilevamento di problemi senza raccomandazioni**

Per motivi di compatibilità, le app possono avere esito negativo in molti modi diversi. PCA rileva molti più problemi di compatibilità rispetto a quelli elencati negli scenari precedenti. In questi casi, molte volte la manifestazione del problema dipende dall'app. Questo significa che alcune app gestiscono normalmente problemi di questo tipo e ne ripristinano, mentre altri no. Quindi, per tali problemi, mentre PCA tiene traccia dell'app, non fornisce una raccomandazione diretta per una correzione.

I problemi rilevati da PCA che non hanno un'impostazione consigliata o una finestra di dialogo includono app che:

-   Hanno un runtime molto breve: le app vengono eseguite per non più di tre secondi
-   Creare oggetti memoria globale senza privilegi amministrativi
-   Errore (eccezione Win32) all'avvio
-   Verifica il privilegio amministrativo (ma potrebbe non riuscire)
-   Usare codec Indeo (deprecato da Windows Vista)
-   Provare a scrivere o eliminare chiavi da percorsi del registro di sistema protetti, ad esempio HKLM
-   Arresto anomalo all'avvio

**Applicazione di correzioni tramite la scheda compatibilità e la risoluzione dei problemi di compatibilità**

Come indicato in precedenza, le app possono avere esito negativo per diversi motivi di compatibilità. Non tutti questi hanno una raccomandazione PCA chiara perché le impostazioni sono dipendenti dall'app. Tuttavia, gli utenti possono passare allo strumento di risoluzione dei problemi di compatibilità o alla scheda compatibilità per applicare alcune correzioni comuni per provare a far funzionare correttamente l'app che ha avuto esito negativo in Windows 8. In questi casi, la PCA rileverà ancora l'app per individuare i problemi di compatibilità, prima e dopo l'applicazione della correzione. Dopo che l'app viene eseguita con la correzione applicata, PCA chiederà all'utente se la correzione ha avuto esito positivo. Quando l'utente risponde alla domanda, i dati vengono inviati in modo anonimo tramite la telemetria a Microsoft. Questi dati vengono raccolti da molti utenti e analizzati e le correzioni valide vengono quindi distribuite in modo esteso a tutti gli utenti di Windows 8 tramite Windows Update.

**Utilizzo dello strumento di risoluzione dei problemi di compatibilità**

Lo strumento di risoluzione dei problemi di compatibilità è un meccanismo di Windows che consente di diagnosticare i problemi delle app e di applicare le correzioni consigliate per il corretto funzionamento. Questa operazione è necessaria solo quando PCA non fornisce alcuna raccomandazione per l'app.

Lo strumento di risoluzione dei problemi consente agli utenti di esaminare e rispondere a una serie di domande e, in base alle risposte, applicherà un set di correzioni e consentirà agli utenti di testare le proprie app e verificare le correzioni. Una volta verificate, le correzioni verranno applicate in modo permanente alle app per renderle più efficaci in Windows 8.

Per informazioni di riferimento, viene visualizzata l'interfaccia utente di risoluzione dei problemi:

![uso della finestra di dialogo Risoluzione dei problemi di compatibilità](images/pcafigure18.png)

È possibile avviare la risoluzione dei problemi di compatibilità in due modi:

**Dalla schermata Start:**

1.  Tipo: risoluzione dei problemi di compatibilità
2.  Nella sezione Impostazioni fare clic sul riquadro ' Esegui programmi eseguiti per la versione precedente di Windows '

  
**Dal riquadro dell'app:**

1.  Dalla schermata Start fare clic con il pulsante destro del mouse sul riquadro dell'app
2.  Fare clic su' Apri percorso file ' (solo app desktop)
3.  Dalla barra multifunzione di Explorer fare clic sulla scheda App
4.  Scegliere ' risoluzione dei problemi di compatibilità'

  


**Uso della scheda compatibilità**

Si noti che questa opzione è consigliata solo agli utenti esperti nel tentativo di impostazioni di compatibilità diverse. Questo metodo non fornisce indicazioni sul tipo di correzione da applicare alle app. Qui è previsto che l'utente conosca quali correzioni possono essere applicate per far funzionare l'app. Se non si è certi delle correzioni, usare lo strumento di risoluzione dei problemi di compatibilità per trovare una correzione per l'app.

Per accedere alla scheda compatibilità:

 **Dalla schermata Start:**

1.  Fare clic con il pulsante destro del mouse sul riquadro app
2.  Apri percorso file (solo app desktop)

  
**Dalla barra multifunzione di Esplora risorse:**

1.  Fare clic su Proprietà
2.  Passare alla scheda compatibilità
3.  Selezionare le correzioni rapide per la compatibilità
4.  Eseguire di nuovo l'app
    > [!Note]  
    > È possibile tornare alla stessa posizione per modificare o rimuovere anche le correzioni. È anche possibile applicare le correzioni a tutti gli utenti nel computer usando il pulsante fornito nella scheda.

     

  


![uso della scheda compatibilità](images/pcafigure19.png)

**App con problemi di compatibilità noti**

Oltre agli scenari di rilevamento dei problemi di runtime elencati sopra, la PCA informa anche gli utenti all'avvio dell'app se l'app presenta problemi di compatibilità noti. L'elenco viene archiviato nel database di compatibilità delle app di sistema. Sono disponibili due tipi di messaggi:

-   **Messaggi di blocco rigido**: se l'app è nota come incompatibile e se si consente l'esecuzione dell'app, si otterrà un grave effetto sul sistema (ad esempio, un arresto anomalo di Windows o non è possibile eseguire l'avvio dopo l'installazione). verrà visualizzato un messaggio di blocco, come illustrato di seguito.

![app con problemi di compatibilità noti-finestra di dialogo dei blocchi rigidi](images/pcafigure20.png)

-   **Messaggi di blocco soft**: se l'app presenta un problema di compatibilità noto e potrebbe non funzionare correttamente, viene visualizzato il messaggio seguente:

![app con problemi di compatibilità noti-finestra di dialogo messaggi di blocco soft](images/pcafigure21.png)

In entrambi i casi, l'opzione ' Ottieni la guida online ' Invia una segnalazione errori Windows per ottenere una risposta in linea da Microsoft e visualizzarla all'utente. In genere, le risposte indirizzano l'utente a uno dei tre tipi di risorse seguenti:

-   Aggiornamento dal fornitore dell'app
-   Sito Web del fornitore dell'app per altre informazioni
-   Un articolo della Microsoft Knowledge base per altre informazioni

**Telemetria per PCA**

Dopo che la PCA risolve tutti i problemi di app in un computer Windows 8 e riceve tutti i commenti e suggerimenti degli utenti, raccoglie i dati anonimi sull'app, il programma di installazione, i problemi rilevati e le impostazioni di compatibilità applicate all'app e le invia nuovamente a Microsoft. Questi dati vengono raccolti da qualsiasi utente che sia disposto a fornire tali dati anonimi (tramite il Analisi utilizzo software analisi utilizzo software). Una volta raccolti questi dati, verranno analizzati gli errori e le correzioni delle app e le correzioni verranno quindi distribuite all'intero ecosistema Windows tramite il meccanismo di Windows Update, in modo che qualsiasi utente dell'app in futuro usufruisca automaticamente della correzione.

**Controlli amministrativi e gestione delle impostazioni PCA**

Gli amministratori IT possono controllare il comportamento PCA in due modi:

-   **Disattiva PCA** : questa impostazione consente agli amministratori IT di disabilitare le finestre di dialogo che la PCA Mostra agli utenti; PCA continuerà a tenere traccia e rilevare i problemi e a inviare dati di telemetria
-   **Disabilitare la telemetria dell'app** : questa impostazione disattiva la raccolta e l'invio dei dati di telemetria da PCA
    > [!Note]  
    > Se analisi utilizzo software è disattivato, questa impostazione non ha alcun effetto.

     

**Progettazione di app per l'uso con PCA**

Gli sviluppatori devono assicurarsi che le proprie app funzionino correttamente in tutti gli scenari di compatibilità descritti in precedenza. Gli sviluppatori devono verificare e convalidare le proprie app per ognuno degli scenari descritti in precedenza e assicurarsi che non vi siano problemi di compatibilità. Se vengono identificati problemi di compatibilità, gli sviluppatori devono apportare le correzioni alle app necessarie per garantire la risoluzione del problema di compatibilità. Di seguito sono riportate alcune delle correzioni comuni che gli sviluppatori devono eseguire:

-   Elimina i controlli della versione del sistema operativo Windows in fase di installazione
-   Elimina controllo dei privilegi (controllo dell'accesso amministratore); usare il manifesto EXE per dichiarare il livello corretto di privilegio necessario
-   Assicurarsi che i file binari di Windows non vengano spediti nel programma di installazione dell'app
-   Elimina la scrittura in aree protette (registro di sistema, cartelle) o scrittura su file protetti
-   Firma digitale di tutti i file binari (EXE, DLL, SYS)
-   Per i programmi di installazione, verificare che sia stata aggiunta la voce ' Aggiungi/Rimuovi programmi ' corretta; come minimo, questa voce di metadati dell'app deve includere il nome dell'app, il server di pubblicazione, la stringa di versione e la lingua supportata. Questo indicherà a PCA che il programma di installazione è stato completato correttamente e fornisce anche un modo pratico per la disinstallazione dell'app

Garantendo che la sezione TRUSTINFO e COMPATIBILITY del manifesto dell'app (eseguibile) venga aggiornata come elencato nella Guida di riferimento per la compatibilità con Windows 8, l'app è stata progettata per Windows 8 e garantisce inoltre che l'app venga sempre eseguita in modalità nativa senza alcuna modalità di compatibilità applicata.

Per assicurarsi che APC consideri l'app per Windows 8:

-   È necessario manifestare tutti i file exe (programma di installazione o Runtime) per le sezioni TRUSTINFO e COMPATIBILITY per Windows 8
-   Il programma di installazione deve aggiungere una voce ' Aggiungi/Rimuovi programmi '

**Glossario**

Le modalità di compatibilità utilizzate da PCA sono elencate di seguito con una breve descrizione di ciò che viene abilitato dalla modalità.



| Mode                         | Descrizione                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Questa modalità emula il comportamento comune di Windows 7, incluso il numero di versione del sistema operativo 6,1                                                                   |
| WindowsVistaSP2              | Questa modalità emula il comportamento comune di Windows 7, incluso il numero di versione del sistema operativo 6,1                                                                   |
| WindowsXPSp3                 | Questa modalità emula il comportamento comune di Windows XP SP3, incluso il numero di versione del sistema operativo 5,1. Include anche la modalità RUNASHIGHEST                    |
| RUNASHIGHEST                 | Questa modalità richiede all'utente di eseguire l'app con il privilegio massimo disponibile. Gli utenti con privilegi amministrativi visualizzeranno una richiesta di elevazione del controllo dell'account utente per l'app |
| RUNASADMIN                   | Questa modalità chiede sempre all'utente di eseguire l'app con privilegi amministrativi. le app con questa modalità otterranno sempre la richiesta di elevazione del controllo dell'account utente                    |
| ELEVATECREATEPROCESS         | Questa modalità consente di eseguire i processi figlio dell'app principale con privilegi amministrativi. i processi figlio otterranno una finestra di dialogo di elevazione del controllo dell'account utente                          |
| PINDLL                       | Questa modalità impone la presenza di una DLL in memoria per un'app anche se l'app Scarica la DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Questa modalità intercetta le eccezioni richiamate dall'utente e consente all'app di continuare senza dover gestire l'eccezione                                          |
| VIRTUALIZEDELETE             | Questa modalità intercetta le operazioni di eliminazione sui file protetti e impedisce l'errore delle app a causa di eccezioni non gestite dell'operazione di eliminazione                   |
| WRPMITIGATION                | Questa modalità restituisce l'esito positivo quando un'app tenta di scrivere, modificare o eliminare i file protetti di Windows o le voci del registro di sistema (senza completare effettivamente l'operazione)  |
| DXMAXIMIZEDWINDOWEDMODE      | Questa modalità identifica le app che passano in modalità schermo intero e le reindirizza in modalità finestra ingrandita                                                          |
| HIGHDPIAWARE                 | Questa modalità consente al resto di Windows di sapere che l'app è compatibile con DPI elevato e consente il rendering appropriato di elementi dell'interfaccia utente, testo, carattere e così via.                              |



 

 

 