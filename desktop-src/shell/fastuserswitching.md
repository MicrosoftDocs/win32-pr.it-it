---
description: Gli account utente di Windows XP consentono l'accesso simultaneo a più utenti, ognuno con le proprie impostazioni e ognuna esegue le proprie applicazioni.
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: Account utente con cambio rapido utente e Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994768"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>Account utente con cambio rapido utente e Desktop remoto

Gli account utente di Windows XP consentono l'accesso simultaneo a più utenti, ognuno con le proprie impostazioni e ognuna esegue le proprie applicazioni. Poiché un utente non deve disconnettersi per consentire l'accesso a un altro utente, è possibile accedere facilmente al desktop di ogni utente utilizzando la funzionalità di cambio rapido utente. Gli account utente includono anche la funzionalità Personal Terminal Server, o Desktop remoto, che consente agli utenti di accedere al proprio account desktop da sistemi remoti.

Vengono illustrati gli argomenti seguenti.

-   [Requisiti di utilizzo dell'infrastruttura](#infrastructure-usage-requirements)
-   [Compatibilità con le applicazioni esistenti](#compatibility-with-existing-applications)
-   [Registrazione per la notifica di cambio della sessione](#registering-for-session-switching-notification)
-   [Verifica dell'esecuzione di una sola istanza dell'applicazione](#ensuring-only-one-instance-of-your-application-is-running)
-   [Chiusura dell'applicazione in tutte le sessioni](#shutting-down-your-application-across-all-sessions)
-   [Interazione con i servizi di sistema](#interaction-with-system-services)
-   [Desktop remoto e larghezza di banda](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>Requisiti di utilizzo dell'infrastruttura

L'infrastruttura sottostante ereditata da Windows 2000 supporta la separazione dello stato dei dati utente, delle impostazioni utente e delle impostazioni del computer. Sfruttando questa infrastruttura, per eseguire correttamente l'applicazione in Windows XP sono necessari gli elementi seguenti.

-   Per impostazione predefinita, la cartella **documenti** per l'archiviazione dei dati creati dall'utente.
-   Classificare e archiviare correttamente i dati dell'applicazione.
-   Degradare normalmente i messaggi "accesso negato".

I file temporanei, i file mappati alla memoria e i documenti devono essere tutti archiviati nella sottodirectory appropriata della directory del profilo dell'utente. Usare [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) per determinare il percorso di archiviazione appropriato per questi file. Il passaggio del flag [**CSIDL \_ AppData**](csidl.md) a queste funzioni restituisce il percorso di una directory file System che funge da repository comune per i dati specifici dell'applicazione. Usare il flag [**CSIDL \_ Local \_ AppData**](csidl.md) al posto di **CSIDL \_ AppData** per i dati che devono essere modificati quando l'utente cambia, ad esempio i file temporanei.

I requisiti elencati sopra sono un subset di quelli del programma di certificazione Microsoft. Per ulteriori informazioni, vedere la pagina **relativa al programma Certified per Windows** in https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx .

## <a name="compatibility-with-existing-applications"></a>Compatibilità con le applicazioni esistenti

Il cambio utente rapido e il Terminal Server personale utilizzano la tecnologia Servizi terminal e pertanto sono compatibili con la maggior parte delle applicazioni Microsoft Win32 più recenti. Se un'applicazione è compatibile con il logo Windows 2000, implementando funzionalità di base per la separazione del profilo e il risparmio di energia, l'applicazione deve essere eseguita correttamente con singoli account utente di Windows XP.

## <a name="registering-for-session-switching-notification"></a>Registrazione per la notifica di cambio della sessione

In genere, non è necessario che un'applicazione riceva una notifica quando si verifica un commutire sul desktop. Tuttavia, le applicazioni che devono ricevere una notifica quando l'account con cui sono in esecuzione sono il desktop corrente, ad esempio le applicazioni che accedono alla porta seriale o ad altre risorse condivise, possono eseguire la registrazione per la notifica del commutere desktop. Per eseguire la registrazione per una notifica, usare la funzione [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) .

Una volta chiamata la funzione, la finestra con handle *HWND* viene registrata per ricevere un messaggio [**di \_ \_ modifica WM WTSSESSION**](../termserv/wm-wtssession-change.md) tramite la funzione **WndProc** . L'ID sessione viene inviato nel parametro **lParam** e un codice che indica l'evento che ha generato il messaggio viene inviato in **wParam** come uno dei flag seguenti.

-   \_connessione della console di WTS \_
-   disconnessione della \_ console WTS \_
-   \_connessione remota \_ WTS
-   \_disconnessione remota WTS \_
-   disconnessione della \_ sessione WTS \_
-   \_accesso alla sessione WTS \_

Le applicazioni possono utilizzare questo messaggio per tenere traccia del proprio stato, nonché per rilasciare e acquisire risorse specifiche della console. I desktop degli utenti possono essere scambiati dinamicamente tra il controllo remoto e la console. Le applicazioni devono usare il messaggio di [**\_ \_ modifica WM WTSSESSION**](../termserv/wm-wtssession-change.md) per eseguire la sincronizzazione con lo stato di connessione locale o remoto.

Quando il processo non richiede più queste notifiche o termina, deve chiamare [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) per annullare la registrazione della notifica.

> [!IMPORTANT]
> I valori **HWND** passati a [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) sono conteggiati come riferimento, quindi è necessario effettuare un numero uguale di chiamate a [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) per garantire il rilascio di tutte le risorse allocate.

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>Verifica dell'esecuzione di una sola istanza dell'applicazione

Molte applicazioni devono assicurarsi che dispongano di una sola istanza in esecuzione. Esistono diversi modi per eseguire questa operazione in Windows XP. Tra le seguenti:

-   Usare [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) o [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) per cercare una finestra Nota che verrà visualizzata dall'applicazione. Se tale finestra è già aperta, è possibile utilizzarla per indicare che l'applicazione è già in esecuzione.
-   Creare un oggetto mutex o Semaphore quando l'applicazione viene aperta e chiudere l'oggetto al termine dell'applicazione. Lo spazio dei nomi dell'oggetto globale è separato per ogni desktop, consentendo un elenco univoco di oggetti mutex e Semaphore per ciascuno di essi.

## <a name="shutting-down-your-application-across-all-sessions"></a>Chiusura dell'applicazione in tutte le sessioni

Potrebbe essere necessario arrestare un'applicazione in tutte le sessioni. Ad esempio, un'applicazione in esecuzione contemporaneamente in due o più sessioni potrebbe scaricare un nuovo file dal Web. Potrebbe quindi essere necessario chiudere e riavviare con i bit aggiornati. Questa operazione, ovviamente, deve essere eseguita in tutte le sessioni in esecuzione. L'applicazione deve essere scritta in modo che venga chiusa quando viene ricevuta una notifica.

## <a name="interaction-with-system-services"></a>Interazione con i servizi di sistema

Da un punto di vista programmatico, è necessario risolvere i casi seguenti.

-   Il processo server riceve una richiesta diretta da un processo client.

    In questo caso, il messaggio viene probabilmente trasmesso tramite una chiamata di procedura locale (LPC) o una chiamata di procedura remota (RPC). Sono disponibili API per LPC o RPC che consentono il recupero del token client. Una volta ottenuto il token client, il server può utilizzarlo in una chiamata a [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera). Questa operazione Visualizza il processo nella finestra della finestra corretta, supponendo che il token dell'utente client disponga di un tag di sessione.

    > [!Note]  
    > Il [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) non supporta la gestione dell'ereditarietà tra le sessioni in questo momento.

     

-   Il processo server riceve una notifica e deve visualizzare l'interfaccia utente, ma non deve essere presente nel contesto dell'utente corrente.

    In questo caso, il processo server può duplicare il token di processo primario e modificare l'identificatore di sessione in questione in modo che corrisponda all'identificatore di sessione corrente. L'identificatore di sessione corrente può essere ottenuto tramite la funzione [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) .

    > [!Note]  
    > Per impostare l'ID di sessione del token, è necessario il **\_ \_ privilegio se TCB**. Questa operazione sarà presente solo come servizio in esecuzione nel sistema NT AUTHORITY \\ .

     

## <a name="remote-desktop-and-bandwidth"></a>Desktop remoto e larghezza di banda

Con l'aggiunta della funzionalità Desktop remoto a Windows XP, le applicazioni devono impegnarsi a non usare una larghezza di banda maggiore di quella necessaria, evitando i disegni di schermate estesi e gli effetti di animazione se il desktop è connesso in remoto. Per determinare se la sessione corrente è remota, è possibile chiamare [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ REMOTESESSION**. Tenere presente, tuttavia, che questa chiamata non distingue tra remote e disconnected.

 

 
