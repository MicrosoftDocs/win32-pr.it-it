---
description: Quando un'applicazione utente richiede dati da oggetti nel sistema tramite un provider WMI, la rappresentazione indica che il provider presenta credenziali che rappresentano il livello di sicurezza dei client anziché i provider.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Rappresentazione di un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b6d1fe931a9e0620643d8b3f8a77c63d031a41f1dac9d17301e11c03d21bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757941"
---
# <a name="impersonating-a-client"></a>Rappresentazione di un client

Quando un'applicazione utente richiede dati da oggetti nel sistema tramite un provider WMI, la rappresentazione indica che il provider presenta credenziali che rappresentano il livello di sicurezza del client anziché quello del provider. La rappresentazione impedisce a un client di ottenere l'accesso non autorizzato alle informazioni nel sistema.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Registrazione di un provider per la rappresentazione](#registering-a-provider-for-impersonation)
-   [Impostazione dei livelli di rappresentazione all'interno di un provider](#setting-impersonation-levels-within-a-provider)
-   [Gestione dei livelli di sicurezza in un provider](#maintaining-security-levels-in-a-provider)
-   [Gestione dei messaggi di accesso negato in un provider](#handling-access-denied-messages-in-a-provider)
-   [Creazione di report di istanze parziali](#reporting-partial-instances)
-   [Segnalazione di enumerazioni parziali](#reporting-partial-enumerations)
-   [Debug del codice di accesso negato](#debugging-your-access-denied-code)
-   [Argomenti correlati](#related-topics)

WMI viene in genere eseguito come servizio amministrativo a un livello di sicurezza elevato, utilizzando il contesto di sicurezza LocalServer. L'uso di un servizio amministrativo consente a WMI di accedere alle informazioni con privilegi. Quando si chiama un provider per ottenere informazioni, WMI passa il relativo ID di sicurezza (SID) al provider, consentendo al provider di accedere alle informazioni allo stesso livello di sicurezza elevato.

Durante il processo di avvio dell'applicazione WMI, il sistema operativo Windows fornisce all'applicazione WMI il contesto di sicurezza dell'utente che ha avviato il processo. Il contesto di sicurezza dell'utente è in genere un livello di sicurezza inferiore rispetto a LocalServer, pertanto l'utente potrebbe non disporre dell'autorizzazione per accedere a tutte le informazioni disponibili per WMI. Quando l'applicazione utente richiede informazioni dinamiche, WMI passa il SID dell'utente al provider corrispondente. Se scritto in modo appropriato, il provider tenta di accedere alle informazioni con il SID dell'utente anziché con il SID del provider.

Per poter rappresentare correttamente l'applicazione client, il provider e l'applicazione client devono soddisfare i criteri seguenti:

-   L'applicazione client deve chiamare WMI con un livello di sicurezza della connessione COM **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE** o **RPC C IMP LEVEL \_ \_ \_ \_ DELEGATE.** Per altre informazioni, vedere [Gestione della sicurezza WMI.](maintaining-wmi-security.md)
-   Il provider deve registrarsi con WMI come provider di rappresentazione. Per altre informazioni, vedere [Registrazione di un provider per la rappresentazione.](#registering-a-provider-for-impersonation)
-   Il provider deve passare al livello di sicurezza dell'applicazione client prima di accedere alle informazioni con privilegi. Per altre informazioni, vedere [Impostazione dei livelli di rappresentazione all'interno di un provider.](#setting-impersonation-levels-within-a-provider)
-   Se l'accesso a queste informazioni viene negato, il provider deve gestire correttamente le condizioni di errore. Per altre informazioni, vedere [Gestione dei messaggi di accesso negato in un provider.](#handling-access-denied-messages-in-a-provider)

## <a name="registering-a-provider-for-impersonation"></a>Registrazione di un provider per la rappresentazione

WMI passa solo il SID di un'applicazione client ai provider registrati come provider di rappresentazione. Per consentire a un provider di eseguire la rappresentazione, è necessario modificare il processo di registrazione del provider.

Nella procedura seguente viene descritto come registrare un provider per la rappresentazione. La procedura presuppone che l'utente comprendi già il processo di registrazione. Per altre informazioni sul processo di registrazione, vedere [Registrazione di un provider.](registering-a-provider.md)

**Per registrare un provider per la rappresentazione**

1.  Impostare la [**proprietà ImpersonationLevel**](swbemsecurity-impersonationlevel.md) della [**\_ \_ classe Win32Provider**](--win32provider.md) che rappresenta il provider su 1.

    La [**proprietà ImpersonationLevel**](swbemsecurity-impersonationlevel.md) indica se il provider supporta o meno la rappresentazione. **L'impostazione di ImpersonationLevel** su 0 indica che il provider non rappresenta il client ed esegue tutte le operazioni richieste nello stesso contesto utente di WMI. **L'impostazione di ImpersonationLevel** su 1 indica che il provider utilizza chiamate di rappresentazione per controllare le operazioni eseguite per conto del client.

2.  Impostare la **proprietà PerUserInitialization** della stessa [**\_ \_ classe Win32Provider**](--win32provider.md) su **TRUE.**

> [!Note]  
> Se si registra un provider con la proprietà **InitializeAsAdminFirst** di [**\_ \_ Win32Provider**](--win32provider.md) impostata su **TRUE,** il provider usa il token di sicurezza del thread a livello di amministrazione solo durante la fase di inizializzazione. Anche se una chiamata [**a CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) non ha esito negativo, il provider usa il contesto di sicurezza di WMI e non del client.

 

Nell'esempio di codice seguente viene illustrato come registrare un provider per la rappresentazione.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Impostazione dei livelli di rappresentazione all'interno di un provider

Se si registra un provider con la proprietà [**impersonationLevel**](swbemsecurity-impersonationlevel.md) della classe [**\_ \_ Win32Provider**](--win32provider.md) impostata su 1, WMI chiama il provider per rappresentare vari client. Per gestire queste chiamate, usare le funzioni COM [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) nell'implementazione dell'interfaccia [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

La [**funzione CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) consente a un server di rappresentare il client che ha effettuato la chiamata. Inserendo una chiamata a **CoImpersonateClient** nell'implementazione di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), si consente al provider di impostare il token di thread del provider in modo che corrisponda al token del thread del client e quindi rappresentare il client. Se non si chiama **CoImpersonateClient**, il provider esegue il codice a livello di amministratore di sicurezza, creando così una potenziale vulnerabilità di sicurezza. Se il provider deve agire temporaneamente come amministratore o eseguire manualmente il controllo di accesso, chiamare [**CoRevertToSelf.**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)

A differenza di [**CoImpersonateClient,**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) è una funzione COM che gestisce i livelli di rappresentazione dei thread. In questo caso, **CoRevertToSelf** riporta il livello di rappresentazione all'impostazione di rappresentazione originale. In generale, il provider è inizialmente un amministratore e alterna **CoImpersonateClient** e **CoRevertToSelf** a seconda che eseressi una chiamata che rappresenta il chiamante o le proprie chiamate. È responsabilità del provider effettuare correttamente queste chiamate in modo da non esporre un problema di sicurezza all'utente finale. Ad esempio, il provider deve chiamare solo funzioni native Windows all'interno della sequenza di codice rappresentato.

> [!Note]  
> Lo scopo di [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) è impostare la sicurezza per un provider. Se si determina che la rappresentazione non è riuscita, è necessario restituire un codice di completamento appropriato a WMI tramite [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Per altre informazioni, vedere [Gestione dei messaggi di accesso negato in un provider.](#handling-access-denied-messages-in-a-provider)

 

## <a name="maintaining-security-levels-in-a-provider"></a>Gestione dei livelli di sicurezza in un provider

I provider non possono chiamare [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) una volta in un'implementazione di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e presuppongono che le credenziali di rappresentazione rimangano valide per la durata del provider. Chiamare invece **CoImpersonateClient** più volte nel corso di un'implementazione per evitare che WMI cambi le credenziali.

Il problema principale per l'impostazione della rappresentazione per un provider è la reentrancy. In questo contesto, la reentrancy si verifica quando un provider effettua una chiamata a WMI per ottenere informazioni e attende che WMI chiami di nuovo il provider. In sostanza, il thread di esecuzione lascia il codice del provider, solo per reim annotarsi il codice in un secondo momento. Reentry fa parte della progettazione di COM e in genere non rappresenta un problema. Tuttavia, quando il thread di esecuzione entra in WMI, il thread assume i livelli di rappresentazione di WMI. Quando il thread torna al provider, è necessario reimpostare i livelli di rappresentazione con un'altra chiamata a [**CoImpersonateClient.**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)

Per proteggersi da problemi di sicurezza nel provider, è necessario effettuare chiamate rientranti in WMI solo durante la rappresentazione del client. Ciò significa che le chiamate a WMI devono essere effettuate dopo aver chiamato [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e prima di [**chiamare CoRevertToSelf.**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) Poiché **CoRevertToSelf** fa in modo che la rappresentazione sia impostata sul livello utente in cui WMI è in esecuzione, in genere le chiamate rientranti a WMI dopo la chiamata a **CoRevertToSelf** potrebbero fornire all'utente e a qualsiasi provider chiamato molte più funzionalità di quelle che dovrebbero avere.

> [!Note]  
> Se si chiama una funzione di sistema o un altro metodo di interfaccia, non è garantito che il contesto di chiamata sia mantenuto.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Gestione dei messaggi di accesso negato in un provider

La maggior parte dei messaggi di errore di accesso negato viene visualizzata quando un client richiede una classe o informazioni a cui non ha accesso. Se il provider restituisce un messaggio di errore di accesso negato a WMI e WMI lo passa al client, il client può dedurre l'esistenza delle informazioni. In alcune situazioni può trattarsi di una violazione della sicurezza. Pertanto, il provider non deve propagare il messaggio al client. Al contrario, il set di classi che il provider avrebbe fornito non deve essere esposto. Analogamente, un provider di istanze dinamiche deve chiamare all'origine dati sottostante per determinare come gestire i messaggi di accesso negato. È responsabilità del provider replicare tale filosofia nell'ambiente WMI. Per altre informazioni, vedere [Creazione di report di istanze parziali](#reporting-partial-instances) e Creazione di report di [enumerazioni parziali.](#reporting-partial-enumerations)

Quando si determina come il provider deve gestire i messaggi di accesso negato, è necessario scrivere ed eseguire il debug del codice. Durante il debug, è spesso utile distinguere tra una negazione a causa di una rappresentazione bassa e una negazione a causa di un errore nel codice. È possibile usare un semplice test nel codice per determinare la differenza. Per altre informazioni, vedere [Debug del codice di accesso negato.](#debugging-your-access-denied-code)

## <a name="reporting-partial-instances"></a>Creazione di report di istanze parziali

Un'occorrenza comune di un messaggio di accesso negato è quando WMI non è in grado di fornire tutte le informazioni necessarie per compilare un'istanza. Ad esempio, un client può avere l'autorità di visualizzare un oggetto unità disco rigido, ma potrebbe non avere l'autorità per visualizzare la quantità di spazio disponibile nell'unità disco rigido stessa. Il provider deve determinare come gestire qualsiasi situazione in cui il provider non è in grado di riempire completamente un'istanza con proprietà a causa di una violazione di accesso.

WMI non richiede una singola risposta ai client con accesso parziale a un'istanza di . WMI versione 1.x consente invece al provider una delle opzioni seguenti:

-   Eseguire l'intera operazione con **WBEM \_ E \_ ACCESS \_ DENIED e** non restituire istanze.

    Restituisce un oggetto errore insieme a **WBEM \_ E \_ ACCESS \_ DENIED** per descrivere il motivo della negazione.

-   Restituire tutte le proprietà disponibili e compilare le proprietà non disponibili con **NULL.**

> [!Note]  
> Assicurarsi che la restituzione di **WBEM \_ E \_ ACCESS \_ DENIED** non crei un problema di sicurezza nell'azienda.

 

## <a name="reporting-partial-enumerations"></a>Segnalazione di enumerazioni parziali

Un'altra occorrenza comune di una violazione di accesso è quando WMI non può restituire tutte le enumerazioni. Ad esempio, un client può avere accesso per visualizzare tutti gli oggetti computer di rete locale, ma potrebbe non avere accesso per visualizzare gli oggetti computer esterni al suo dominio. Il provider deve determinare come gestire qualsiasi situazione in cui non è possibile completare un'enumerazione a causa di una violazione di accesso.

Come per un provider di istanze, WMI non richiede una singola risposta a un'enumerazione parziale. WMI versione 1.x consente invece a un provider una delle opzioni seguenti:

-   Restituisce **WBEM \_ S NO \_ \_ ERROR** per tutte le istanze a cui il provider può accedere.

    Se si usa questa opzione, l'utente non è a conoscenza del fatto che alcune istanze non erano disponibili. Diversi provider, ad esempio quelli che usano Structured Query Language (SQL) con sicurezza a livello di riga, restituiscono risultati parziali riusciti usando il livello di sicurezza del chiamante per definire il set di risultati.

-   Eseguire l'intera operazione **con WBEM \_ E ACCESS \_ \_ DENIED** e non restituire istanze.

    Il provider può includere facoltativamente un oggetto errore che descrive la situazione per il client. Si noti che alcuni provider possono accedere alle origini dati in modo seriale e possono riscontrare negazioni solo in parte tramite l'enumerazione .

-   Restituisce tutte le istanze a cui è possibile accedere, ma restituisce anche il codice di stato non di errore **WBEM \_ S \_ ACCESS \_ DENIED**.

    Il provider deve prendere nota della negazione durante l'enumerazione e può continuare a fornire istanze, finendo con il codice di stato nonerror. Il provider può anche scegliere di terminare l'enumerazione alla prima negazione. La giustificazione di questa opzione è che provider diversi hanno paradigmi di recupero diversi. Un provider potrebbe aver già recapitato istanze prima di individuare una violazione di accesso. Alcuni provider possono scegliere di continuare a fornire altre istanze e altri potrebbero voler terminare.

A causa della struttura di COM, non è possibile eseguire il marshalling di informazioni durante un errore, ad eccezione di un oggetto errore. Pertanto, non è possibile restituire sia informazioni che un codice di errore. Se si sceglie di restituire informazioni, è necessario usare un codice di stato non di errore.

## <a name="debugging-your-access-denied-code"></a>Debug del codice di accesso negato

Alcune applicazioni possono usare livelli di rappresentazione inferiori a **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE**. In questo caso, la maggior parte delle chiamate di rappresentazione effettuate dal provider per l'applicazione client avrà esito negativo. Per progettare e implementare correttamente un provider, è necessario tenere presente questa idea.

Per impostazione predefinita, l'unico altro livello di rappresentazione che può accedere a un provider è **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY**. Nei casi in cui un'applicazione client usa **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY,** [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) non restituisce un codice di errore. Al contrario, il provider rappresenta il client solo a scopo di identificazione. Pertanto, la maggior Windows metodi chiamati dal provider restituirà un messaggio di accesso negato. Questo è innocuo nella pratica, in quanto gli utenti non saranno autorizzati a eseguire operazioni inappropriati. Tuttavia, può essere utile durante lo sviluppo del provider sapere se il client è stato effettivamente rappresentato o meno.

Il codice richiede i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come determinare se un provider ha rappresentato correttamente un'applicazione client.


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> </dl>

 

 
