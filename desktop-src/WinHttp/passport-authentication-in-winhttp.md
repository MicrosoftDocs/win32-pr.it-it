---
description: Microsoft Windows i servizi HTTP (WinHTTP) supportano completamente l'uso lato client del protocollo Microsoft Passport di autenticazione. In questo argomento viene fornita una panoramica delle transazioni coinvolte nell'autenticazione Passport e viene illustrato come gestirle.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Autenticazione Passport in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d6aff7f8924c307d4e21efb77bc57ebae2469e50361b57d12dce5b348555e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114317"
---
# <a name="passport-authentication-in-winhttp"></a>Autenticazione Passport in WinHTTP

Microsoft Windows i servizi HTTP (WinHTTP) supportano completamente l'uso lato client del protocollo Microsoft Passport di autenticazione. In questo argomento viene fornita una panoramica delle transazioni coinvolte nell'autenticazione Passport e viene illustrato come gestirle.

> [!Note]  
> In WinHTTP 5.1 l'autenticazione Passport è disabilitata per impostazione predefinita.

 

## <a name="passport-14"></a>Passport 1.4

Passport è un componente fondamentale dei servizi Microsoft .NET blocchi predefiniti. Consente alle aziende di sviluppare e offrire servizi Web distribuiti in un'ampia gamma di applicazioni e consente ai membri di usare un solo nome di accesso e una sola password in tutti i siti Web partecipanti.

WinHTTP fornisce il supporto della piattaforma Microsoft Passport 1.4 implementando il protocollo lato client per l'autenticazione Passport 1.4. Libera le applicazioni dai dettagli dell'interazione con l'infrastruttura Passport e i nomi utente e le password archiviati in Windows XP. Questa astrazione fa sì che l'uso di Passport non sia diverso dal punto di vista dello sviluppatore rispetto all'uso di schemi di autenticazione tradizionali come Basic o Digest.

**Windows XP:** La chiave del Registro di sistema **HKCU \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet Impostazioni Passport \\ \\ \\ NumRegistrationRuns** identifica il numero di volte in cui viene visualizzata l'Autenticazione guidata Passport quando è richiesta l'autenticazione PassPort. Se il valore di questa chiave è impostato su un numero maggiore di 5, la procedura guidata non viene visualizzata.

Le sezioni seguenti descrivono le transazioni coinvolte nell'autenticazione Passport dal punto di vista di un'applicazione client. Per lo sviluppo di Passport sul lato server, vedere La panoramica della documentazione di Passport SDK.

-   [Richiesta iniziale](#initial-request)
-   [Server di accesso Passport](#passport-login-server)
-   [Richiesta autenticata](#authenticated-request)

### <a name="initial-request"></a>Richiesta iniziale

Quando un client richiede una risorsa in un server che richiede l'autenticazione Passport, il server verifica la presenza di [*ticket*](glossary.md). Se viene inviato *un ticket* valido con la richiesta, il server risponde con la risorsa richiesta. Se il *ticket* non esiste nel client, il server risponde con un codice di stato 302. La risposta include l'intestazione della richiesta, "WWW-Authenticate: Passport1.4". I client che non usano Passport possono seguire il reindirizzamento al server di accesso Passport. I client più avanzati in genere contattano passport nexus per determinare la posizione del server di accesso Passport.

> [!Note]  
> La rete di Microsoft Passport è il Passport *Nexus,* che facilita la sincronizzazione dei siti dei partecipanti Passport per garantire che ogni sito abbia i dettagli più recenti sulla configurazione di rete e altri problemi. Ogni componente Passport (Passport Manager, server di accesso, server di aggiornamento e così via) comunica periodicamente con Nexus per recuperare le informazioni necessarie per individuare e comunicare correttamente con gli altri componenti nella rete Passport. Queste informazioni vengono recuperate come documento XML denominato documento di configurazione dei componenti o CCD.

 

L'immagine seguente mostra la richiesta iniziale a un'affiliata Passport.

![l'immagine mostra la richiesta iniziale a un'affiliata passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Server di accesso Passport

Un server di accesso Passport gestisce tutte le richieste di [*ticket per*](glossary.md) qualsiasi risorsa in un'autorità di *dominio* Passport. Prima che una richiesta possa essere autenticata tramite Passport, l'applicazione client deve contattare il server di accesso per ottenere i *ticket appropriati.*

Quando un client richiede [*ticket*](glossary.md) a un server di accesso Passport, il server di accesso in genere risponde con un codice di stato 401 per indicare che è necessario fornire le credenziali utente. Quando vengono fornite queste credenziali, il server di accesso risponde con i *ticket* necessari per accedere alla risorsa specificata nel server che contiene la risorsa richiesta in origine. Il server di accesso può anche reindirizzare il client a un altro server che può fornire la risorsa richiesta.

![l'immagine mostra una richiesta di ticket client a un server di accesso Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Richiesta autenticata

Quando il client ha i [*ticket*](glossary.md) che corrispondono a un determinato server, tali *ticket* vengono inclusi in tutte le richieste a tale server. Se i *ticket* non sono stati modificati da quando sono  stati recuperati dal server di accesso Passport e i ticket sono validi per il server delle risorse, il server delle risorse invia una risposta che include sia la risorsa richiesta che i cookie che indicano che l'utente è autenticato per le richieste future.

I cookie aggiuntivi nella risposta hanno lo scopo di velocizzare il processo di autenticazione. Le richieste aggiuntive nella stessa sessione per le risorse nei server nella stessa autorità di dominio Passport includono tutti questi cookie aggiuntivi. Non è necessario inviare di nuovo le credenziali al server di accesso fino alla scadenza dei cookie.

![l'immagine mostra una richiesta autenticata al server di accesso passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Uso di Passport in WinHTTP

L'autenticazione Passport in WinHTTP è molto simile ad altri schemi di autenticazione. Vedere [Autenticazione in WinHTTP](authentication-in-winhttp.md) per una panoramica dell'autenticazione in WinHTTP.

In WinHTTP 5.1 l'autenticazione Passport è disabilitata per impostazione predefinita e deve essere abilitata in modo esplicito [**con WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) prima dell'uso.

WinHTTP gestisce internamente molti dettagli della transazione per l'autenticazione Passport. Durante la richiesta iniziale, il server risponde con un codice di stato 302 quando è necessaria l'autenticazione. Il codice di stato 302 indica effettivamente un reindirizzamento e fa parte del protocollo Passport per la compatibilità con le versioni precedenti. WinHTTP nasconde il codice di stato 302 e contatta passport nexus e quindi il server di accesso. All'applicazione WinHTTP viene notificato il codice di stato 401 inviato dal server di accesso per richiedere le credenziali utente. Per l'applicazione, tuttavia, viene visualizzato come se lo stato 401 proviene dal server da cui è stata richiesta la risorsa. In questo modo, l'applicazione WinHTTP non è a conoscenza delle interazioni con altri server e può gestire l'autenticazione Passport con lo stesso codice che gestisce altri schemi di autenticazione.

In genere, un'applicazione WinHTTP risponde a un codice di stato 401 fornendo le credenziali di autenticazione. Quando le credenziali vengono fornite con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**SetCredentials**](iwinhttprequest-setcredentials.md) per l'autenticazione Passport, le credenziali vengono effettivamente inviate al server di accesso, non al server indicato nella richiesta.

Tuttavia, quando si risponde a un codice di stato 407, un'applicazione WinHTTP deve usare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire le credenziali proxy, anziché [**WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Poiché **WinHttpSetOption** è un modo meno sicuro per fornire le credenziali, in genere è consigliabile evitarlo.

Una volta recuperati, [*i ticket*](glossary.md) vengono gestiti internamente e inviati automaticamente ai server applicabili nelle richieste future.

> [!Note]  
> WinHTTP consente di disabilitare il reindirizzamento automatico chiamando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per il flag [**WINHTTP \_ OPTION DISABLE \_ \_ FEATURE**](option-flags.md) e specificando il valore [**WINHTTP DISABLE \_ \_ REDIRECTS.**](option-flags.md) La disabilitazione del reindirizzamento non interferisce con il reindirizzamento gestito internamente da WinHTTP per le transazioni Passport.

 

WinHTTP può completare correttamente l'autenticazione Passport anche se un'applicazione disabilita il reindirizzamento automatico. Tuttavia, al termine dell'autenticazione Passport, è necessario eseguire un reindirizzamento implicito dall'URL del server di accesso Passport all'URL originale. Questo reindirizzamento non viene attivato da una risposta HTTP 302, ma è implicito nel protocollo Passport.

WinHTTP gestisce questo reindirizzamento implicito in modo speciale. Se un'applicazione ha disabilitato il reindirizzamento automatico, WinHTTP richiede che l'applicazione conserti a WinHTTP "l'autorizzazione" per il reindirizzamento automatico in questo caso speciale.

Per fare in modo che WinHTTP reindirizza all'URL originale dopo l'autenticazione, l'applicazione deve registrare una funzione di callback [**usando WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) WinHTTP può quindi inviare una notifica all'applicazione con un callback DI REINDIRIZZAMENTO STATO CALLBACK WINHTTP, che consente \_ all'applicazione di annullare il \_ \_ reindirizzamento. Un'applicazione non deve fornire alcuna funzionalità nella funzione di callback. La registrazione del callback è sufficiente per consentire a WinHTTP di seguire questo reindirizzamento caso speciale.

Il messaggio ERROR \_ WINHTTP \_ LOGIN FAILURE viene generato se una funzione di callback non è \_ impostata dall'applicazione.

### <a name="passport-cobranding"></a>Passport Cobranding

A differenza degli schemi di autenticazione tradizionali supportati da WinHTTP, Passport può essere [*ampiamente supportato con .*](glossary.md) Quando si riceve un codice di stato 401 che indica una richiesta di verifica, un'applicazione può recuperare l'elemento grafico e il testo di *cobranding.* Recuperare un URL per *l'immagine di cobranding* chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con il \_ flag \_ DELL'URL \_ COBRANDING WINHTTP OPTION \_ PASSPORT. Recuperare il *testo di cobranding* chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con il \_ flag WINHTTP OPTION PASSPORT \_ \_ COBRANDING \_ TEXT. Questi elementi possono essere usati per personalizzare una finestra di dialogo di raccolta delle credenziali.

### <a name="stored-user-names-and-passwords"></a>Gestione nomi utente e password archiviati

Windows XP ha introdotto il concetto di nomi utente e password archiviati. Se le credenziali Passport di un utente vengono salvate tramite la Registrazione guidata **Passport** o la finestra di dialogo delle credenziali **standard,** queste vengono salvate in Nomi utente e password archiviati. Quando si usa WinHTTP in Windows XP o versioni successive, WinHTTP usa automaticamente le credenziali in Nomi utente e password archiviati se le credenziali non sono impostate in modo esplicito. È simile al supporto delle credenziali di accesso predefinite per NTLM/Kerberos. Tuttavia, l'uso delle credenziali Passport predefinite non è soggetto alle impostazioni dei criteri di accesso automatico.

### <a name="disabling-passport-authentication"></a>Disabilitazione dell'autenticazione Passport

Alcune applicazioni potrebbero richiedere la possibilità di disabilitare l'autenticazione Passport. Ad esempio, quando un'affiliata Passport risponde con il codice di stato 302 iniziale, potrebbe essere preferibile seguire il reindirizzamento indicato ed eseguire il rendering della pagina di autenticazione PASSPORT HTML anziché consentire a WinHTTP di gestire internamente l'autenticazione. L'autenticazione Passport è disabilitata in WinHTTP chiamando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione WINHTTP OPTION CONFIGURE PASSPORT AUTH e passando il valore \_ \_ \_ \_ WINHTTP \_ DISABLE PASSPORT \_ \_ AUTH. Può essere ri abilitata in un secondo momento con WINHTTP \_ ENABLE \_ PASSPORT \_ AUTH.

L'autenticazione Passport non può essere disabilitata quando si usa [**l'oggetto WinHttpRequest.**](winhttprequest.md)

Come specificato in precedenza in questa sezione, l'autenticazione Passport è disabilitata per impostazione predefinita in WinHTTP 5.1 e deve essere abilitata in modo esplicito [**con WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) prima dell'uso.

## <a name="passport-configuration-overrides-used-for-testing"></a>Override della configurazione passport usati per i test

WinHTTP si basa sulle informazioni di configurazione scaricate dal server Passport Nexus per supportare l'autenticazione Passport 1.4. Per impostazione predefinita, questo server sicuro (SSL) è nexus.passport.com e la risorsa di configurazione è rdr/pprdr.asp, nota come configurazione passport "live". Il formato delle informazioni è un'intestazione HTTP personalizzata "PassportURLs", seguita da coppie attributo-valore delimitate da virgole.

Ad esempio, " https://nexus.passport.com/rdr/pprdr.asp " restituisce le informazioni di configurazione seguenti:

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

Le parti rilevanti per WinHTTP sono DARealm, DALogin e ConfigVersion. Per motivi di prestazioni, vengono memorizzati nella cache per la durata di una sessione WinHTTP. Questi tre valori possono essere sostituiti dalle applicazioni necessarie per lavorare con un'altra infrastruttura Passport diversa dalla configurazione di produzione "live" modificando le impostazioni del Registro di sistema appropriate in

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

Se LoginServerUrl è presente nel Registro di sistema, WinHTTP non contatta il server Nexus per altri valori di configurazione. In questo caso, anche LoginServerRealm e ConfigVersion devono essere impostati tramite il Registro di sistema per i valori corretti.

Un'applicazione può, a scopo di test, essere necessaria per scaricare la configurazione passport da un server Nexus privato. Questa operazione può essere eseguita eseguendo l'override di due valori del Registro di sistema in

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

 

 



