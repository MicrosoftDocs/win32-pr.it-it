---
title: Scenari di Assistente compatibilità programmi per Windows 8
description: Scenari di Assistente compatibilità programmi per Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63fbd912e14ac682ffe820ad140b2cad6a487dfbac833aa419c53389a9339ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852595"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Scenari di Assistente compatibilità programmi per Windows 8

## <a name="platforms"></a>Piattaforme

**Client** - Windows XP \| Windows Vista Windows \| 7 \| Windows 8  

## <a name="description"></a>Descrizione

Program Compatibility Assistant (PCA) è una funzionalità di Windows 8 che consente agli utenti finali di eseguire app desktop progettate per le versioni Windows precedenti. Windows 8 offre una compatibilità delle app integrata che consente alle app progettate per Windows 7 o versioni precedenti Windows di funzionare in modo Windows 8 automatico. Tuttavia, è presente un numero ridotto di app che possono avere problemi di esecuzione senza intervento.

Quando un utente esegue un'app, PCA tiene traccia dell'app e identifica eventuali sintomi di determinati problemi di compatibilità noti in Windows 8. Quando rileva eventuali sintomi di problema, offre all'utente la possibilità di applicare una correzione consigliata che consente di eseguire meglio l'app Windows 8.

## <a name="scenarios"></a>Scenari

PCA tiene traccia delle app per un set di problemi di compatibilità noti in Windows 8. PCA tiene traccia dei problemi, identifica le correzioni e fornisce all'utente una finestra di dialogo con le istruzioni per applicare una correzione consigliata. L'utente può decidere di applicare le correzioni consigliate o scegliere di non eseguire alcuna operazione e annullare la raccomandazione. Se l'utente annulla l'operazione, PCA non tiene più traccia dell'app.

PCA applica in genere una delle tre modalità di compatibilità Windows: Windows XP SP3, Windows Vista SP2 o Windows 7, a seconda della data di creazione del programma o della relativa configurazione. PCA usa gli attributi LINK DATE e SUBSYSTEM VERSION del programma e le sezioni TRUSTINFO e COMPATIBILITY del manifesto del file eseguibile per determinare quale delle modalità è rilevante e si applica \_ rispettivamente Windows XP SP3 (include privilegi amministrativi), Windows Vista SP2 o Windows 7. Un glossario alla fine del documento elenca ognuna delle modalità di compatibilità applicate da PCA e la relativa descrizione.

Per tutti gli scenari elencati di seguito, PCA tiene traccia delle app per la seconda volta dopo l'applicazione di una correzione. Se l'app continua a non riuscire nello stesso modo anche dopo l'applicazione di una correzione di compatibilità, PCA ripristina la correzione. PCA interromperà quindi in modo permanente il rilevamento dell'app specifica che ha avuto esito negativo.

Sebbene PCA tiene traccia di molti potenziali problemi, non tutti i problemi causeranno effettivamente errori dell'app. PCA consiglia le correzioni solo in situazioni in cui esiste un'elevata probabilità che l'errore dell'app sia dovuto a Windows di compatibilità. Le sezioni seguenti si espandono in ognuno degli scenari PCA sviluppati in Windows 8. Ogni sezione descrive lo scenario del problema e le raccomandazioni fornite da PCA per consentire all'app di continuare a funzionare correttamente Windows 8.

Per altre informazioni sulle modifiche di compatibilità in Windows 8, vedere gli altri argomenti della guida Windows 8 *compatibility cookbook*.

Gli scenari a cui PCA tiene traccia e consiglia le correzioni sono:

-   L'app non riesce a installare o disinstallare
-   L'app non viene eseguita con un messaggio Windows di controllo della versione
-   L'app non viene avviata a causa di privilegi amministrativi
-   Arresto anomalo dell'app a causa di problemi di memoria specifici
-   L'app non riesce a causa di file di sistema non corrispondenti
-   L'app ha esito negativo a causa di errori non gestiti in Windows
-   L'app non riesce durante il tentativo di eliminare i file non Windows protetti
-   L'app non riesce durante il tentativo di modificare Windows file
-   L'app non riesce a causa dell'uso di modalità a colori a 8 o 16 bit
-   L'app non riesce a causa di problemi di grafica e visualizzazione
-   L'app non riesce a dichiarare il riconoscimento DPI
-   L'app non riesce a causa della mancanza Windows funzionalità
-   L'app ha esito negativo a causa di driver non firmati in Windows 8
-   Rilevamento delle app installate tramite le impostazioni di compatibilità
-   L'app non avvia programmi di installazione o programmi di aggiornamento
-   Programmi di installazione delle app che devono essere eseguiti con privilegi amministrativi
-   Apple Pannello di controllo legacy che devono essere eseguite con privilegi amministrativi

Ognuno di questi scenari è espanso di seguito:

**L'app non riesce a installare o disinstallare**

Uno dei tipi più comuni di errori dell'app si verifica durante l'installazione dell'app. I programmi di installazione meno recenti in genere hanno esito negativo in due modi:

-   Il programma di installazione non è a conoscenza delle funzionalità di Controllo dell'account utente in Windows 8, pertanto potrebbe non essere eseguito con i privilegi completi necessari per apportare modifiche di sistema alle aree protette di Windows 8
-   Il programma di installazione verifica la versione Windows e blocca l'esecuzione se la versione è superiore a quella prevista

Queste condizioni di errore sono due dei tipi più comuni di errori di compatibilità durante l'installazione. PCA, con l'aiuto di vari altri componenti Windows, ad esempio controllo dell'account utente, rileva i programmi di installazione all'avvio e li tiene traccia fino alla fine dell'installazione. Se il programma di installazione non riesce ad aggiungere file o ad aggiungere una voce valida nella parte "Installazione applicazioni" del pannello di controllo di Windows, PCA considera l'installazione non riuscita.

In questo caso, PCA consiglia una modalità di compatibilità appropriata per l'app. La modalità di compatibilità consente l'esecuzione del programma di installazione in modalità Windows per cui è stata progettata e garantisce anche che l'app venga eseguita con privilegi amministrativi. PCA applica la modalità di compatibilità RUNASADMIN insieme alla modalità di compatibilità Windows XP, Windows Vista o Windows 7. L'utente, al termine dell'installazione non riuscita, visualizza una finestra di dialogo con la raccomandazione PCA:

![l'app non riesce a installare o disinstallare la finestra di dialogo](images/pcafigure1.png)

L'utente può quindi scegliere di:

-   Eseguire il programma usando le impostazioni di compatibilità (opzione consigliata), dopo di che PCA applierà l'impostazione consigliata (modalità di compatibilità), riavvia il programma di installazione e lo tiene traccia fino al completamento dell'installazione
-   Indicare che il programma è installato correttamente, nel qual caso PCA non aggiungerà alcuna impostazione e interromperà il rilevamento dell'installazione
-   Fare clic su Chiudi, nel qual caso PCA non aggiungerà alcuna impostazione e interromperà il rilevamento di questa configurazione

Lo stesso meccanismo viene usato per facilitare la disinstallazione dell'app quando un utente tenta di disinstallare l'app dalla sezione "Installazione applicazioni" in Windows o dal collegamento del programma di disinstallazione dell'app.

**L'app non viene eseguita con un messaggio Windows di controllo della versione**

Uno degli errori di compatibilità più comuni nel runtime dell'app è dovuto al controllo Windows versione. Molte app, al momento dell'avvio, controllano Windows versione. se non riconoscono la versione, si bloccano anche se l'app potrebbe essere stata eseguita senza problemi.

In genere, questi controlli sono associati a due condizioni che il PCA tiene traccia:

L'app visualizza una finestra di messaggio che avvisa l'utente. Di seguito è riportato un esempio:

![L'app non viene eseguita con una finestra di dialogo del messaggio di controllo della versione di Windows](images/pcafigure2.png)

-   L'app termina immediatamente o si arresta in modo anomalo

Se PCA identifica entrambe queste condizioni per un'app, fornirà una raccomandazione all'utente. PCA consentirà all'utente di eseguire nuovamente l'app con le impostazioni di compatibilità. PCA applica la modalità di compatibilità Windows XP, Windows Vista o Windows 7 appropriata in base all'app. Come in qualsiasi scenario, l'utente può indicare a PCA che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante chiudi. Di seguito è riportata una finestra di dialogo di esempio:

![l'app non viene eseguita con una finestra di dialogo di messaggio di controllo della versione di Windows](images/pcafigure3.png)

**L'app non viene avviata o eseguita a causa di privilegi amministrativi**

Alcune app necessitano di privilegi amministrativi per eseguire ed eseguire le funzionalità. Tuttavia, in Windows 8, come Windows 7 e Windows Vista, le app vengono eseguite con livelli di privilegi inferiori per impostazione predefinita a causa del controllo dell'account utente. Le app più recenti progettate per Windows Vista e versioni successive dichiarano in genere il livello di privilegio che devono eseguire usando la sezione TRUSTINFO del manifesto EXE. Tuttavia, le app meno recenti in genere hanno esito negativo in due modi:

-   L'app visualizza un messaggio per l'utente che richiede privilegi amministrativi, come illustrato di seguito:

![L'app non viene avviata o eseguita a causa di una finestra di dialogo con privilegi amministrativi](images/pcafigure4a.png)

-   L'app termina immediatamente o si arresta in modo anomalo

Se PCA identifica entrambe queste condizioni per un'app, fornirà una raccomandazione all'utente. PCA consentirà all'utente di eseguire nuovamente l'app con privilegi amministrativi .PCA applica la modalità di compatibilità RUNASHIGHEST. L'utente riceverà una richiesta di controllo dell'account utente quando l'app viene rieseguiti. Come in qualsiasi scenario, l'utente può scegliere di eseguire di nuovo con l'impostazione consigliata o rifiutare esplicitamente le impostazioni consigliate facendo clic su Chiudi. Di seguito è riportata una finestra di dialogo di esempio:

![L'app non viene avviata o eseguita a causa della finestra di dialogo dell'opzione dei privilegi amministrativi](images/pcafigure5.png)

**Arresto anomalo dell'app a causa di problemi di memoria specifici**

Alcune app si arrestano in modo anomalo a causa di un problema noto di memoria. L'app de-fa riferimento a una DLL dalla memoria e quindi chiama una funzione per eseguire codice nella stessa DLL. Ciò causa un arresto anomalo immediato dell'app. Anche se questo problema non è dovuto Windows 8 di compatibilità, è un problema relativamente comune che si verifica in un'ampia gamma di app. PCA tiene traccia di questo problema per offrire agli utenti la possibilità di eseguire l'app in modo più affidabile.

Per queste app, PCA applica automaticamente la modalità di compatibilità PINDLL in modo invisibile all'utente. La modalità di compatibilità richiamata da PCA impedisce all'app di liberare la DLL dalla memoria. Pertanto, la chiamata di funzione nella DLL da parte dell'app funzionerà, impedendo l'arresto anomalo dell'app e consentendo di continuare a funzionare correttamente.

**L'app ha esito negativo a causa di file di sistema non corrispondenti**

Alcune app progettate per Windows XP e versioni precedenti includono copie Windows DLL di sistema con i relativi programmi di installazione. Quando tali app vengono installate, l'app ha sia una copia precedente della DLL nella propria cartella che la versione più recente della DLL presente nelle cartelle di sistema Windows.

In Windows Vista e versioni successive questa condizione può causare un errore dell'app quando tenta di caricare la DLL locale, poiché questa DLL non funzionerà correttamente con le altre DLL di sistema Windows corrente. Poiché l'app in genere non è a conoscenza delle versioni più recenti di questa DLL, non funziona correttamente.

Quando l'amministratore di sistema rileva che la DLL non è stata caricata correttamente, applica un'impostazione di compatibilità che consente a Windows di caricare la versione più recente della DLL dalla cartella di sistema Windows in modo che l'app possa essere eseguita correttamente.

Al termine della prima esecuzione non riuscita dell'app, gli utenti visualizzano la finestra di dialogo PCA che notifica l'impostazione applicata come indicato di seguito:

![L'app non riesce a causa della mancata corrispondenza della finestra di dialogo dei file di sistema](images/pcafigure6.png)

**L'app ha esito negativo a causa di errori non gestiti nelle applicazioni a 64 bit Windows**

Nella versione a 64 bit di Windows 8 è stata abilitata una nuova eccezione per il meccanismo di callback del ciclo di messaggi. Anche se questa eccezione è stata introdotta per la Windows 7, non era obbligatorio gestire questo errore. In Windows 8, le app che usano cicli di messaggi devono gestire questa nuova eccezione. In caso contrario, si arresteranno in modo anomalo. Le app progettate per Windows versioni precedenti potrebbero non essere a conoscenza di questa eccezione e pertanto potrebbero non gestire correttamente questo errore (eccezione).

PCA rileva le app che hanno esito negativo a causa di questo errore non gestito e applica automaticamente la modalità di compatibilità DISABLEUSERCALLBACKEXCEPTION per l'app. Dopo aver applicato l'impostazione alla fine dell'esecuzione, l'utente viene informato come indicato di seguito. L'app otterrà la modalità all'esecuzione successiva e sarà in grado di evitare questo errore.

![L'app non riesce a causa di errori non gestiti nella finestra di dialogo di Windows a 64 bit](images/pcafigure7.png)

**L'app ha esito negativo durante il tentativo di eliminare file non Windows protetti**

Alcune app progettate per Windows XP e precedenti presuppongono che siano in genere eseguite con privilegi amministrativi completi. Come comportamento normale delle app, possono provare a eliminare i file non Windows protetti (in file di programma o Windows cartelle). Quando l'operazione di eliminazione ha esito negativo, molte app di questo tipo possono bloccarsi.

PcA rileva queste app che non riescono a eliminare i file protetti e si arresta in modo anomalo e fornisce una raccomandazione all'utente. PcA consentirà all'utente di eseguire nuovamente l'app con le impostazioni di compatibilità. Come in qualsiasi scenario, l'utente può indicare all'account del servizio di gestione delle app che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante Chiudi. In questo caso PCA applica la modalità di compatibilità VIRTUALIZEDELETE. Di seguito è riportato un dialogo di esempio:

![L'app ha esito negativo durante il tentativo di eliminare la finestra di dialogo file non Windows protetti](images/pcafigure8.png)

**L'app ha esito negativo durante il tentativo di modificare Windows file o chiavi del Registro di sistema**

Alcune app progettate per Windows XP e precedenti presuppongono che siano in genere eseguite con privilegi amministrativi completi. Come comportamento normale delle app, possono provare a modificare, eliminare o scrivere file protetti Windows (in file di programma o cartelle Windows) o chiavi del Registro di sistema di proprietà di Windows. Quando un'operazione di scrittura, eliminazione o modifica per un file o una chiave del Registro di sistema ha esito negativo, molte app di questo tipo possono bloccarsi o avere esito negativo.

PcA rileva queste app che non riescono a scrivere nei file Windows protetti o nelle chiavi del Registro di sistema e fornisce una raccomandazione all'utente alla chiusura dell'app. PcA consentirà all'utente di eseguire nuovamente l'app con le impostazioni di compatibilità. Come in qualsiasi scenario, l'utente può indicare all'account del servizio di gestione delle app che l'app è stata eseguita correttamente o rifiutare esplicitamente le impostazioni consigliate facendo clic sul pulsante Chiudi. In questo caso pcA applica la modalità di compatibilità WRPMITIGATION. Di seguito è riportato un dialogo di esempio:

![L'app ha esito negativo durante il tentativo di modificare i file di Windows o la finestra di dialogo delle chiavi del Registro di sistema](images/pcafigure9.png)

**L'app ha esito negativo a causa dell'uso delle modalità colore a 8 o 16 bit**

Come parte della ridefinizione del Windows 8 per le app di Windows Store, una delle principali modifiche è che il Gestione finestre desktop (DWM) supporterà ora solo i colori a 32 bit in Windows 8. Le modalità di colore inferiori sono ora simulate.

Molti giochi e app meno recenti progettati per Windows XP o versioni precedenti usano le modalità colore a 8 bit o a 16 bit. Senza mitigazioni, queste app potrebbero non essere eseguite in Windows 8. Tuttavia, quando queste app enumerano o provano a usare una delle modalità di colore a 8 o 16 bit per la visualizzazione, PCA identifica immediatamente il problema e, con l'aiuto di DWM, garantisce che l'app funzioni correttamente con la modalità colore simulata.

Si noti che questa situazione si verifica non appena l'app richiede le modalità a colori basso ed è trasparente per l'utente. L'utente non deve riavviare l'app per ottenere questa mitigazione perché questa correzione è sempre necessaria per garantire il corretto funzionamento dell'app.

**L'applicazione non riesce a causa di problemi di grafica e visualizzazione**

Poiché Gestione finestre desktop (DWM) è sempre attiva in Windows 8, alcune app precedenti dell'era Windows XP possono avere esito negativo se l'app usa API grafiche in modalità mista, come nell'uso delle API GDI e DirectX per disegnare sullo schermo (principalmente giochi meno recenti) e tenta di usare la modalità schermo intero:

-   DWM impedirà il disegno direttamente sul desktop e il gioco o l'app avrà esito negativo oppure disegna una schermata nera sul desktop e nessuna grafica sarà visibile
-   In questi casi, quando l'app viene chiuso, Windows rileva che l'app o il gioco presenta un problema con la modalità schermo intero e applica la modalità di compatibilità DXMAXIMIZEDWINDOWEDMODE che consente l'esecuzione dell'app o del gioco in modalità finestra ingrandita anziché in modalità schermo intero
-   Dopo che l'impostazione è stata applicata alla fine dell'esecuzione, l'utente viene informato da PCA come illustrato di seguito. l'app otterrà la modalità di compatibilità all'esecuzione successiva e potrà essere eseguita correttamente

![L'applicazione ha esito negativo a causa di problemi di grafica e visualizzazione della finestra di dialogo](images/pcafigure10.png)

**L'app non riesce a dichiarare la consapevolezza DPI**

Un altro tipico problema di visualizzazione con molte app meno recenti si verifica quando Windows e l'app viene eseguita in modalità DPI elevato, ma l'app non dichiara la propria consapevolezza del valore DPI elevato tramite il manifesto EXE. Tra i problemi comuni che possono verificarsi a causa di questa mancata corrispondenza nelle impostazioni vi sono elementi o testo dell'interfaccia utente ritagliati e dimensioni del carattere non corrette. Per altre informazioni sui problemi, vedere questo collegamento [qui.](/previous-versions//dd464660(v=vs.85))

In questi casi, Windows rileva che l'app è compatibile con valori DPI elevati e applica la modalità di compatibilità HIGHDPIAWARE all'app alla fine della prima esecuzione. PcA informerà quindi l'utente su questo come illustrato di seguito:

![L'app non riesce a dichiarare la finestra di dialogo di riconoscimento dpi](images/pcafigure11.png)

**L'applicazione non riesce a causa di funzionalità Windows mancanti**

Alcune app dipendono Windows funzionalità che sono state rimosse dopo Windows Vista. Quando queste app tentano di caricare le DLL o i componenti COM mancanti, non funzionano.

PcA rileva le app quando tenta di caricare le funzionalità Windows mancanti e fornisce un consiglio per scaricare questi componenti e installarli al termine dell'app. L'utente può fare clic su "Get Help Online" (Ottieni guida online) per trovare un'alternativa o scaricare la funzionalità e installarla. Se necessario, l'utente può scegliere di non eseguire alcuna operazione facendo clic su Chiudi.

![L'applicazione ha esito negativo a causa di una finestra di dialogo delle funzionalità di Windows mancante](images/pcafigure12.png)

**L'app ha esito negativo a causa di driver non firmati in un Windows 8**

I driver Windows a 64 bit hanno richiesto driver con firma digitale (file SYS) Windows Vista. Tuttavia, le app precedenti progettate prima del rilascio di Windows driver forniti da Vista che non erano firmati digitalmente. Se tale driver non firmato è installato, Windows non li carica. In rari casi, è possibile che Windows non si avvia se tali driver sono contrassegnati come driver in fase di avvio.

Alcune app meno recenti installano driver non firmati a 64 bit Windows. Qualsiasi dispositivo o app che tenta di usare questo driver potrebbe non riuscire o causare un arresto anomalo del sistema. Per evitare questo scenario, PCA rileva le app quando installano driver non firmati e disabilita il driver contrassegnato come driver in fase di avvio.

Indica inoltre all'utente di acquisire un driver con firma digitale per il corretto funzionamento dell'app. Il messaggio viene visualizzato come risultato dell'installazione del driver e come risultato dell'installazione dell'app. Se un'altra app installa lo stesso driver, anche l'app riceverà lo stesso messaggio.

![L'app non riesce a causa di driver non firmati nella finestra di dialogo di Windows 8 a 64 bit](images/pcafigure13.png)

**Rilevamento delle app installate tramite le impostazioni di compatibilità**

Quando un programma di installazione non riesce, PCA consente al programma di installazione di eseguire varie modalità di compatibilità a seconda del tipo di errore. Quando il programma di installazione ha esito positivo con le impostazioni di compatibilità, PCA tiene traccia dei collegamenti aggiunti dal programma di installazione. Questa operazione viene eseguita per rilevare se le app installate potrebbero richiedere anche le impostazioni di compatibilità applicate al programma di installazione.

Quando un utente avvia un'app di questo tipo, PCA chiede all'utente di chiedere se l'app funziona correttamente. Se l'utente risponde "Sì", l'A PCA interrompe il rilevamento dell'app. Se l'utente risponde "No", applica la stessa modalità di compatibilità applicata al programma di installazione dell'app ed esegue nuovamente l'app con la modalità di compatibilità applicata.

**L'app non avvia programmi di installazione o aggiornamenti**

Le app talvolta avviano programmi figlio che devono essere eseguiti come amministratori. Questo è in genere il caso in cui un'app tenta di avviare il software di aggiornamento per controllare e installare nuovi aggiornamenti nell'app. Quando le app eseguono direttamente tali programmi figlio, il programma figlio può non essere avviato perché l'app stessa non dispone di privilegi amministrativi o perché il programma figlio non è stato contrassegnato correttamente per l'elevazione con il manifesto di Controllo dell'account utente.

PcA tiene traccia di questi errori e alla chiusura dell'app primaria applica automaticamente la modalità di compatibilità ELEVATECREATEPROCESS che consente l'esecuzione corretta dei programmi figlio. Quando l'app avvia l'app figlio nelle esecuzioni successive, l'utente visualizza una finestra di dialogo di controllo dell'account utente per il programma figlio.

Di seguito è riportato un esempio della finestra di dialogo PCA:

![L'app non riesce ad avviare i programmi di installazione o la finestra di dialogo degli aggiornamenti](images/pcafigure14.png)

**Programmi di installazione app che devono essere eseguiti con privilegi amministrativi**

I programmi di Windows applicazioni desktop richiedono privilegi amministrativi perché scrivono file, cartelle e voci del Registro di sistema in aree di sistema protette. Windows dispone di logica di rilevamento per identificare quando viene eseguito un programma di installazione e chiede immediatamente all'utente di fornire privilegi amministrativi tramite la finestra di dialogo controllo dell'account utente. Tuttavia, in alcuni casi, questa logica non sarà in grado di determinare che un'app è effettivamente un programma di installazione e potrebbe non ottenere privilegi amministrativi. Si tratta in genere di programmi di installazione personalizzati che non usano tecnologie di installazione note, ad esempio Windows o Install Shield.

In questi casi, PCA rileva che il programma di installazione non è riuscito a scrivere i file. Al termine dell'installazione non riuscita, l'A PCA fornirà una raccomandazione per applicare le impostazioni di compatibilità. Se l'utente sceglie di fare clic su "Esegui programma", l'amministratore di sistema applierà la modalità di compatibilità RUNASADMIN ed eseguirà nuovamente il programma di installazione. Se l'utente sceglie di chiudere, non verrà applicata alcuna impostazione. Di seguito è riportata una finestra di dialogo PCA di esempio:

![Screenshot che mostra un esempio di finestra di dialogo per un programma di installazione di app che deve essere eseguito con privilegi amministrativi.](images/pcafigure15.png)

Le Pannello di controllo applet legacy che devono essere eseguite con privilegi amministrativi Le applet del Pannello di controllo modificano in genere le impostazioni di sistema e necessitano della possibilità di eseguire l'amministratore di annunci. Tuttavia, quelli scritti prima Windows Vista non hanno un manifesto EXE o non dispongono della sezione TRUSTINFO che dichiara il livello di privilegio richiesto. Quando si eseguono queste applet, l'autorità di gestione delle applicazioni (PCA) le rileva e, alla fine della prima esecuzione, fornisce una raccomandazione per l'esecuzione con le impostazioni amministrative. Se l'utente sceglie di fare clic su "Esegui programma", PCA applica la modalità di compatibilità RUNASADMIN ed esegue nuovamente il programma di installazione. Se l'utente sceglie di chiudere, non verrà applicata alcuna impostazione. Di seguito è riportata una finestra di dialogo PCA di esempio:

![Programmi di installazione app che devono essere eseguiti con la finestra di dialogo dei privilegi amministrativi](images/pcafigure16.png)

**Verifica delle impostazioni consigliate tramite commenti e suggerimenti degli utenti**

Alla fine di ognuno degli scenari (dopo l'esecuzione dell'app con le impostazioni di compatibilità consigliate), PCA pone all'utente una semplice domanda:

![verifica delle impostazioni consigliate tramite la finestra di dialogo commenti e suggerimenti degli utenti](images/pcafigure17.png)

L'utente può inviare commenti e suggerimenti se l'app ha funzionato o ha avuto esito negativo con l'impostazione di compatibilità. Questi dati verranno inviati in modo anonimo a Microsoft. In questo modo è possibile garantire che tali correzioni possano essere integrate in Windows 8 tramite il processo di aggiornamento di Windows, in modo che gli utenti futuri di Windows 8 non rilevino più l'errore dell'app e l'account del servizio di gestione delle app non dovrà più tenere traccia dell'errore dell'app.

**Rilevamento dei problemi che non hanno raccomandazioni**

Le app possono non riuscire in molti modi diversi per motivi di compatibilità. PcA tiene traccia di molti più problemi di compatibilità rispetto a quanto elencato negli scenari precedenti. In questi casi, spesso il problema dipende dall'app. Ciò significa che alcune app gestiscono questi problemi normalmente e ne recuperano le informazioni, mentre altre potrebbero non farlo. Pertanto, per questi problemi, mentre l'A PCA tiene traccia dell'app, non fornisce una raccomandazione diretta per una correzione.

I problemi che PCA rileva che non hanno un'impostazione consigliata o una finestra di dialogo includono le app che:

-   Avere un runtime molto breve: le app vengono eseguite per un massimo di tre secondi
-   Creare oggetti di memoria globali senza privilegi amministrativi
-   Genera un errore (eccezione Win32) all'avvio
-   Verificare la presenza di privilegi amministrativi (ma potrebbe non avere esito negativo)
-   Usare codec Indeo (deprecati da Windows Vista)
-   Provare a scrivere o eliminare chiavi da percorsi del Registro di sistema protetti, ad esempio HKLM
-   Arresto anomalo all'avvio

**Applicazione di correzioni tramite la scheda Compatibilità e lo strumento di risoluzione dei problemi di compatibilità**

Come accennato in precedenza, le app possono avere esito negativo per diversi motivi di compatibilità. Non tutti questi elementi hanno una chiara raccomandazione pcA perché le impostazioni dipendono dall'app. Tuttavia, gli utenti possono passare a Risoluzione dei problemi di compatibilità o alla scheda Compatibilità per applicare alcune correzioni comuni per provare a ottenere il corretto funzionamento dell'app in Windows 8. In questi casi, l'A PCA tiene comunque traccia dell'app per i problemi di compatibilità, prima e dopo l'applicazione della correzione. Dopo l'esecuzione dell'app con la correzione applicata, l'A PCA chiederà all'utente se la correzione ha funzionato. Quando l'utente risponde alla domanda, i dati vengono inviati in modo anonimo tramite i dati di telemetria a Microsoft. Questi dati vengono raccolti da molti utenti e analizzati e le correzioni idonee vengono quindi distribuite su larga Windows 8 utenti tramite Windows aggiornamento.

**Uso dello strumento di risoluzione dei problemi di compatibilità**

Lo strumento di risoluzione dei problemi di compatibilità è un meccanismo Windows che consente di diagnosticare i problemi con le app e applicare le correzioni consigliate per il corretto funzionamento. Questa operazione è necessaria solo quando l'A PCA non fornisce alcuna raccomandazione per l'app.

Lo strumento di risoluzione dei problemi consente agli utenti di eseguire e rispondere a un set di domande e, in base alle risposte, applierà un set di correzioni e consentirà agli utenti di testare le app e verificare le correzioni. Dopo la verifica, le correzioni verranno applicate in modo permanente alle app per renderle più Windows 8.

L'interfaccia utente dello strumento di risoluzione dei problemi è illustrata di seguito per riferimento:

![uso della finestra di dialogo dello strumento di risoluzione dei problemi di compatibilità](images/pcafigure18.png)

È possibile avviare lo strumento di risoluzione dei problemi di compatibilità in due modi:

**Dalla schermata Start:**

1.  Tipo: strumento di risoluzione dei problemi di compatibilità
2.  Nella sezione settings (Impostazioni) fare clic sul riquadro "Run programs made for previous version of Windows" (Esegui programmi per la versione precedente Windows'

  
**Dal riquadro dell'app:**

1.  Nell'elenco schermata Start fare clic con il pulsante destro del mouse sul riquadro dell'app
2.  Fare clic su "Apri percorso file" (solo app desktop)
3.  Nella barra multifunzione di Explorer fare clic sulla scheda App
4.  Scegliere "Risoluzione dei problemi di compatibilità"

  


**Uso della scheda Compatibilità**

Si noti che questa opzione è consigliata solo per gli utenti esperti che provano impostazioni di compatibilità diverse. Questo metodo non fornisce alcuna raccomandazione sul tipo di correzione da applicare alle app. In questo caso è previsto che l'utente sappia quali correzioni possono essere applicate per il funzionamento dell'app. Se non si è certi delle correzioni, usare lo strumento di risoluzione dei problemi di compatibilità per trovare una correzione per l'app.

Per accedere alla scheda Compatibilità:

 **Dalla schermata Start:**

1.  Fare clic con il pulsante destro del mouse sul riquadro dell'app
2.  Apri percorso file (solo app desktop)

  
**Dalla barra multifunzione di Explorer:**

1.  Fare clic su Proprietà
2.  Passare alla scheda Compatibilità
3.  Selezionare le correzioni per la compatibilità
4.  Eseguire nuovamente l'app
    > [!Note]  
    > È possibile tornare nella stessa posizione anche per modificare o rimuovere le correzioni. È anche possibile applicare le correzioni a tutti gli utenti nel computer usando il pulsante disponibile nella scheda.

     

  


![uso della scheda di compatibilità](images/pcafigure19.png)

**App con problemi di compatibilità noti**

Oltre agli scenari di rilevamento dei problemi di runtime elencati in precedenza, PCA informa anche gli utenti all'avvio dell'app se l'app presenta problemi di compatibilità noti. L'elenco viene archiviato nel database di compatibilità delle app di sistema. Esistono due tipi di questi messaggi:

-   Messaggi di blocco hardware: se l'app è nota come incompatibile e se si consente l'esecuzione dell'app si verifica un grave impatto sul sistema (ad esempio, un arresto anomalo del Windows o l'impossibilità di avviarsi dopo l'installazione), verrà visualizzato un messaggio di blocco come illustrato di seguito

![App con problemi di compatibilità noti - finestra di dialogo dei messaggi a blocchi rigidi](images/pcafigure20.png)

-   **Messaggi di blocco soft:** se l'app presenta un problema di compatibilità noto e potrebbe non funzionare correttamente, viene visualizzato questo messaggio:

![App con problemi di compatibilità noti - finestra di dialogo dei messaggi di blocco soft](images/pcafigure21.png)

In entrambi i casi, l'opzione "Ottieni assistenza online" invia una segnalazione errori Windows per ottenere una risposta online da Microsoft e visualizzarla all'utente. In genere le risposte puntano l'utente a uno dei tre tipi di risorse seguenti:

-   Un aggiornamento del fornitore dell'app
-   Sito Web di un fornitore di app per altre informazioni
-   Per altre informazioni, vedere l'articolo della Microsoft Knowledge Base

**Telemetria per PCA**

Dopo che l'account pcA risolve i problemi dell'app in un computer Windows 8 e riceve tutti i commenti e suggerimenti degli utenti, raccoglie dati anonimi sull'app, il programma di installazione, i problemi rilevati e le impostazioni di compatibilità applicate all'app e invia i dati a Microsoft. Questi dati vengono raccolti da qualsiasi utente disposto a fornire tali dati anonimi (tramite il Analisi utilizzo software - Analisi utilizzo software). Dopo aver raccolto questi dati, gli errori e le correzioni dell'app vengono analizzati e le correzioni vengono quindi distribuite all'intero ecosistema di Windows tramite il meccanismo di aggiornamento di Windows in modo che qualsiasi utente dell'app in futuro traa vantaggio automaticamente dalla correzione.

**Controlli amministrativi e gestione delle impostazioni PCA**

Gli amministratori IT possono controllare il comportamento di PCA in due modi:

-   **Disattiva PCA:** questa impostazione consente agli amministratori IT di disattivare le finestre di dialogo visualizzate dall'amministratore PCA agli utenti. L'analisi pcA continuerà a rilevare e rilevare i problemi e a inviare nuovamente i dati di telemetria
-   **Disattiva i dati di telemetria** dell'app: questa impostazione disattiva qualsiasi raccolta e invio di dati di telemetria da parte di PCA
    > [!Note]  
    > Se Analisi utilizzo software è disattivato, questa impostazione non ha alcun impatto.

     

**Progettazione di app per l'uso con PCA**

Gli sviluppatori devono assicurarsi che le app funzionino correttamente in tutti gli scenari di compatibilità descritti in precedenza. Gli sviluppatori devono testare e convalidare le app per ognuno degli scenari precedenti e assicurarsi che non siano presenti problemi di compatibilità. Se vengono identificati problemi di compatibilità, gli sviluppatori devono apportare le correzioni necessarie alle proprie app per assicurarsi che il problema di compatibilità sia risolto. Alcune delle correzioni comuni che gli sviluppatori devono apportare includono:

-   Eliminare i Windows della versione del sistema operativo in fase di installazione e di runtime
-   Eliminare il controllo dei privilegi (verifica dell'accesso come amministratore); usare il manifesto EXE per dichiarare il livello di privilegio necessario
-   Assicurarsi che i Windows binari non siano forniti all'interno del programma di installazione dell'app
-   Eliminare la scrittura in aree protette (Registro di sistema, cartelle) o la scrittura su file protetti
-   Firma digitale di tutti i file binari (file EXE, DLL, SYS)
-   Per i programmi di installazione, assicurarsi che sia stata aggiunta la voce "Installazione applicazioni" appropriata. Come minimo, questa voce di metadati dell'app deve includere il nome dell'app, l'editore, la stringa della versione e la lingua supportata. Questo indicherà all'A PCA che il programma di installazione è stato completato correttamente e fornirà agli utenti un modo pratico per disinstallare l'app

Verificando che la sezione TRUSTINFO e COMPATIBILITY del manifesto dell'app (eseguibile) venga aggiornata come indicato nella guida di riferimento alla compatibilità di Windows 8, l'analisi pca indica che l'app è stata progettata per Windows 8 e garantisce anche che l'app venga sempre eseguita in modo nativo senza alcuna modalità di compatibilità applicata.

Per assicurarsi che PCA consideri l'app come progettata per Windows 8:

-   Tutte le ESE (programma di installazione o runtime) devono essere manifeste per le sezioni TRUSTINFO e COMPATIBILITY per Windows 8
-   Il programma di installazione deve aggiungere una voce "Installazione applicazioni"

**Glossario**

Le modalità di compatibilità usate da PCA sono elencate di seguito con una breve descrizione delle funzionalità abilitate dalla modalità.



| Mode                         | Descrizione                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Questa modalità emula il comportamento Windows 7, incluso il numero di versione del sistema operativo 6.1                                                                   |
| WindowsVistaSP2              | Questa modalità emula il comportamento Windows 7, incluso il numero di versione del sistema operativo 6.1                                                                   |
| WindowsXPSp3                 | Questa modalità emula Windows comportamento di XP SP3, incluso il numero di versione del sistema operativo 5.1. È inclusa anche la modalità RUNASHIGHEST                    |
| RUNASHIGHEST                 | Questa modalità richiede all'utente di eseguire l'app con il privilegio più elevato disponibile. Gli utenti con privilegi amministrativi visualizzano una richiesta di elevazione dei privilegi di Controllo dell'account utente per l'app |
| RUNASADMIN                   | Questa modalità richiede sempre all'utente di eseguire l'app con privilegi amministrativi. Le app con questa modalità riceveranno sempre la richiesta di elevazione dei privilegi di Controllo dell'account utente                    |
| ELEVATECREATEPROCESS         | Questa modalità consente l'esecuzione dei processi figlio dell'app principale con privilegi amministrativi. I processi figlio otterrà una finestra di dialogo di elevazione dei privilegi di Controllo dell'account utente                          |
| PINDLL                       | Questa modalità forza una DLL a essere in memoria per un'app anche se l'app scarica la DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Questa modalità intercetta le eccezioni di richiamo dell'utente e consente all'app di continuare senza dover gestire l'eccezione                                          |
| VIRTUALIZEDELETE             | Questa modalità intercetta le operazioni di eliminazione sui file protetti e impedisce alle app di avere esito negativo a causa di eccezioni non gestite dall'operazione di eliminazione                   |
| WRPMITIGATION                | Questa modalità restituisce l'esito positivo quando un'app tenta di scrivere, modificare o eliminare Windows file protetti o voci del Registro di sistema (senza completare effettivamente l'operazione)  |
| DXMAXIMIZEDWINDOWEDMODE      | Questa modalità identifica le app che passano alla modalità schermo intero e le reindirizza in modalità finestra ingrandita                                                          |
| HIGHDPIAWARE                 | Questa modalità consente al resto del Windows di sapere che l'app è in grado di riconoscere valori DPI alti e consente il rendering corretto di elementi dell'interfaccia utente, testo, tipo di carattere e così via.                              |



 

 

 