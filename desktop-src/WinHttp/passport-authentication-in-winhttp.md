---
description: I servizi HTTP di Microsoft Windows (WinHTTP) supportano completamente l'utilizzo da parte del client del protocollo di autenticazione Microsoft Passport. In questo argomento viene fornita una panoramica delle transazioni relative all'autenticazione Passport e alla relativa modalità di gestione.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Autenticazione Passport in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8fc00217c7c14fbd4635fab68398d2056c1ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484181"
---
# <a name="passport-authentication-in-winhttp"></a>Autenticazione Passport in WinHTTP

I servizi HTTP di Microsoft Windows (WinHTTP) supportano completamente l'utilizzo da parte del client del protocollo di autenticazione Microsoft Passport. In questo argomento viene fornita una panoramica delle transazioni relative all'autenticazione Passport e alla relativa modalità di gestione.

> [!Note]  
> In WinHTTP 5,1, Passport Authentication è disabilitato per impostazione predefinita.

 

## <a name="passport-14"></a>Passport 1,4

Passport è un componente di base del Microsoft .NET servizi di blocco predefinito. Consente alle aziende di sviluppare e offrire servizi Web distribuiti in un'ampia gamma di applicazioni e consente ai suoi membri di usare un nome di accesso e una password in tutti i siti Web partecipanti.

WinHTTP fornisce supporto della piattaforma per Microsoft Passport 1,4 implementando il protocollo sul lato client per l'autenticazione Passport 1,4. Consente di liberare le applicazioni dai dettagli sull'interazione con l'infrastruttura Passport e i nomi utente e le password archiviati in Windows XP. Questa astrazione rende l'uso di Passport non diverso dal punto di vista dello sviluppatore rispetto all'uso di schemi di autenticazione tradizionali come Basic o digest.

**Windows XP:** La chiave del registro di sistema **HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings \\ Passport \\ NumRegistrationRuns** identifica il numero di volte in cui viene visualizzata la procedura guidata autenticazione Passport quando è richiesta l'autenticazione Passport. Se il valore di questa chiave è impostato su un numero maggiore di 5, la procedura guidata non viene visualizzata.

Nelle sezioni seguenti vengono descritte le transazioni relative all'autenticazione Passport dal punto di vista di un'applicazione client. Per lo sviluppo di Passport sul lato server, vedere Cenni preliminari sulla documentazione di Passport SDK.

-   [Richiesta iniziale](#initial-request)
-   [Server di accesso Passport](#passport-login-server)
-   [Richiesta autenticata](#authenticated-request)

### <a name="initial-request"></a>Richiesta iniziale

Quando un client richiede una risorsa in un server che richiede l'autenticazione Passport, il server controlla la richiesta di presenza di [*ticket*](glossary.md). Se viene inviato un *ticket* valido con la richiesta, il server risponde con la risorsa richiesta. Se il *ticket* non esiste nel client, il server risponde con un codice di stato 302. La risposta include l'intestazione della richiesta "WWW-Authenticate: Passport 1.4". I client che non usano Passport possono seguire il reindirizzamento al server di accesso Passport. I client più avanzati in genere contattano Passport Nexus per determinare la posizione del server di accesso Passport.

> [!Note]  
> La rete centrale per la Microsoft Passport è Passport *Nexus*, che facilita la sincronizzazione dei siti dei partecipanti al passaporto, per garantire che ogni sito disponga dei dettagli più recenti sulla configurazione di rete e altri problemi. Ogni componente Passport (gestione Passport, server di accesso, server di aggiornamento e così via) comunica periodicamente con il Nexus per recuperare le informazioni necessarie per individuare e comunicare correttamente con gli altri componenti nella rete Passport. Queste informazioni vengono recuperate come documento XML denominato documento di configurazione del componente o CCD.

 

Nell'immagine seguente viene illustrata la richiesta iniziale a un affiliato Passport.

![Image Mostra la richiesta iniziale a un affiliato Passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Server di accesso Passport

Un server di accesso Passport gestisce tutte le richieste di [*ticket*](glossary.md) per qualsiasi risorsa in un' *autorità di dominio* Passport. Prima di poter autenticare una richiesta tramite Passport, l'applicazione client deve contattare il server di accesso per ottenere i *ticket* appropriati.

Quando un client richiede [*ticket*](glossary.md) da un server di accesso Passport, il server di accesso risponde in genere con un codice di stato 401 per indicare che è necessario fornire le credenziali utente. Quando vengono fornite queste credenziali, il server di accesso risponde con i *ticket* necessari per accedere alla risorsa specificata nel server che contiene la risorsa originariamente richiesta. Il server di accesso può anche reindirizzare il client a un altro server che può fornire la risorsa richiesta.

![Image Mostra una richiesta di ticket client a un server di accesso Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Richiesta autenticata

Quando il client dispone di [*ticket*](glossary.md) che corrispondono a un determinato server, i *ticket* sono inclusi in tutte le richieste al server. Se i *ticket* non sono stati modificati dopo che sono stati recuperati dal server di accesso Passport e i *ticket* sono validi per il server di risorse, il server delle risorse invia una risposta che include sia la risorsa richiesta che i cookie che indicano che l'utente è autenticato per richieste future.

I cookie aggiuntivi nella risposta hanno lo scopo di velocizzare il processo di autenticazione. Le richieste aggiuntive nella stessa sessione per le risorse nei server della stessa autorità di dominio Passport includono tutte questi cookie aggiuntivi. Non è necessario che le credenziali vengano inviate nuovamente al server di accesso fino alla scadenza dei cookie.

![Image Mostra una richiesta autenticata al server di accesso Passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Uso di Passport in WinHTTP

L'autenticazione Passport in WinHTTP è molto simile ad altri schemi di autenticazione. Per una panoramica dell'autenticazione in WinHTTP, vedere [autenticazione in WinHTTP](authentication-in-winhttp.md) .

In WinHTTP 5,1, l'autenticazione Passport è disabilitata per impostazione predefinita e deve essere abilitata in modo esplicito con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) prima dell'uso.

WinHTTP gestisce molti dettagli della transazione internamente per l'autenticazione Passport. Durante la richiesta iniziale, il server risponde con un codice di stato 302 quando è necessaria l'autenticazione. Il codice di stato 302 indica effettivamente un reindirizzamento ed è parte del protocollo Passport per la compatibilità con le versioni precedenti. WinHTTP nasconde il codice di stato 302 e Contatta Passport Nexus, quindi il server di accesso. L'applicazione WinHTTP riceve una notifica del codice di stato 401 inviato dal server di accesso per richiedere le credenziali utente. Per l'applicazione, tuttavia, viene visualizzato come se lo stato 401 proviene dal server da cui è stata richiesta la risorsa. In questo modo, l'applicazione WinHTTP non è a conoscenza delle interazioni con altri server e può gestire l'autenticazione Passport con lo stesso codice che gestisce altri schemi di autenticazione.

In genere, un'applicazione WinHTTP risponde a un codice di stato 401 fornendo le credenziali di autenticazione. Quando vengono fornite le credenziali [](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) con WinHttpSetCredentials [**o le credenziali per**](iwinhttprequest-setcredentials.md) l'autenticazione Passport, le credenziali vengono effettivamente inviate al server di accesso, non al server indicato nella richiesta.

Tuttavia, quando si risponde a un codice di stato 407, un'applicazione WinHTTP deve usare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire le credenziali proxy, anziché [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Poiché **WinHttpSetOption** è un modo meno sicuro per fornire le credenziali, in genere dovrebbe essere evitato.

Una volta recuperati, [*i ticket*](glossary.md) vengono gestiti internamente e vengono inviati automaticamente ai server applicabili nelle richieste future.

> [!Note]  
> WinHTTP consente di disabilitare il reindirizzamento automatico chiamando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per l' [**opzione WinHTTP Disabilita il flag di \_ \_ \_ funzionalità**](option-flags.md) e SPECIFICAndo il valore [**WinHTTP \_ Disable \_ reindirizzas**](option-flags.md). La disabilitazione del reindirizzamento non interferisce con il reindirizzamento che WinHTTP gestisce internamente per le transazioni Passport.

 

WinHTTP può completare correttamente l'autenticazione Passport anche se un'applicazione Disabilita il reindirizzamento automatico. Tuttavia, al termine dell'autenticazione Passport, un reindirizzamento implicito deve ricorrere dall'URL del server di accesso Passport all'URL originale. Questo reindirizzamento non viene attivato da una risposta HTTP 302, ma è implicito nel protocollo Passport.

WinHTTP gestisce questo reindirizzamento implicito in modo specifico. Se un'applicazione ha disabilitato il reindirizzamento automatico, WinHTTP richiede che l'applicazione conferisca l'autorizzazione "WinHTTP" per il reindirizzamento automatico in questo caso speciale.

Per fare in modo che WinHTTP ritorni all'URL originale dopo l'autenticazione, l'applicazione deve registrare una funzione di callback usando [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback). WinHTTP può quindi inviare una notifica all'applicazione con \_ un \_ callback di reindirizzamento dello stato di callback WinHTTP \_ , che consente all'applicazione di annullare il reindirizzamento. Non è necessario che un'applicazione fornisca alcuna funzionalità nella funzione di callback. la registrazione del callback è sufficiente per consentire a WinHTTP di seguire questo reindirizzamento speciale.

Il \_ \_ \_ messaggio di errore di accesso WinHTTP di errore viene generato se una funzione di callback non è impostata dall'applicazione.

### <a name="passport-cobranding"></a>Personalizzazione del passaporto

A differenza degli schemi di autenticazione tradizionali supportati da WinHTTP, Passport può essere esteso a una [*nuova personalizzazione*](glossary.md). Quando si riceve un codice di stato 401 che indica una richiesta di verifica, un'applicazione può recuperare l'immagine e il testo del *marchio* . Recuperare un URL per l'immagine di *cobranding* chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con il \_ \_ \_ flag URL di personalizzazione dell'opzione WinHTTP \_ . Recuperare il testo di *cobranding* chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con il flag del testo per l' \_ opzione WinHTTP \_ Passport \_ cobranding \_ . Questi elementi possono essere utilizzati per personalizzare una finestra di dialogo di raccolta delle credenziali.

### <a name="stored-user-names-and-passwords"></a>Gestione nomi utente e password archiviati

In Windows XP è stato introdotto il concetto di nomi utente e password archiviati. Se le credenziali Passport di un utente vengono salvate tramite la **registrazione guidata Passport** o la **finestra di dialogo credenziali** standard, vengono salvate in nomi utente e password archiviati. Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali nei nomi utente e nelle password archiviati se le credenziali non sono impostate in modo esplicito. Questa operazione è simile a quella del supporto per le credenziali di accesso predefinite per NTLM/Kerberos. Tuttavia, l'utilizzo delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.

### <a name="disabling-passport-authentication"></a>Disabilitazione dell'autenticazione Passport

Alcune applicazioni potrebbero richiedere la possibilità di disabilitare l'autenticazione Passport. Ad esempio, quando un affiliato Passport risponde con il codice di stato iniziale 302, potrebbe essere preferibile seguire il reindirizzamento indicato ed eseguire il rendering della pagina di autenticazione HTML Passport anziché consentire a WinHTTP di gestire l'autenticazione internamente. L'autenticazione Passport è disabilitata in WinHTTP chiamando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l' \_ opzione WinHTTP \_ Configure \_ Passport \_ AUTH e passando il valore WinHTTP \_ Disable \_ Passport \_ auth. Può essere riabilitata in un secondo momento con WINHTTP \_ enable \_ Passport \_ auth.

Non è possibile disabilitare l'autenticazione Passport quando si usa l'oggetto [**WinHttpRequest**](winhttprequest.md) .

Come indicato in precedenza in questa sezione, l'autenticazione Passport è disabilitata per impostazione predefinita in WinHTTP 5,1 e deve essere abilitata in modo esplicito con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) prima dell'uso.

## <a name="passport-configuration-overrides-used-for-testing"></a>Override della configurazione Passport usati per il test

WinHTTP si basa sulle informazioni di configurazione scaricate dal server Passport Nexus per supportare l'autenticazione Passport 1,4. Per impostazione predefinita, questo server protetto (SSL) è nexus.passport.com e la risorsa di configurazione è rdr/pprdr. asp, nota come configurazione Passport "Live". Il formato delle informazioni è costituito da un'intestazione HTTP personalizzata "PassportURLs", seguita da coppie attributo-valore delimitate da virgole.

"", Ad esempio, https://nexus.passport.com/rdr/pprdr.asp restituisce le informazioni di configurazione seguenti:

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

Le parti rilevanti per WinHTTP sono DARealm, DALogin e ConfigVersion. Per motivi di prestazioni, vengono memorizzati nella cache per la durata di una sessione WinHTTP. Questi tre valori possono essere sostituiti dalle applicazioni necessarie per lavorare con un'altra infrastruttura Passport diversa dalla configurazione di produzione "attiva" modificando le impostazioni del registro di sistema appropriate in

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

Se LoginServerUrl è presente nel registro di sistema, WinHTTP non contatta il server Nexus per altri valori di configurazione. In questo caso, è necessario impostare anche LoginServerRealm e ConfigVersion tramite il registro di sistema per correggere i valori.

Un'applicazione può, a scopo di test, essere necessaria per scaricare la configurazione Passport da un server Nexus privato. Questa operazione può essere eseguita eseguendo l'override di due valori del registro di sistema in

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione in WinHTTP](authentication-in-winhttp.md)
</dt> </dl>

 

 



