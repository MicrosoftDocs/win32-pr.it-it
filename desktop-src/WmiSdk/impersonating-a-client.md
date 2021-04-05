---
description: Quando un'applicazione utente richiede dati da oggetti nel sistema tramite un provider WMI, la rappresentazione significa che il provider presenta le credenziali che rappresentano il livello di sicurezza dei client anziché i provider.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Rappresentazione di un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883533"
---
# <a name="impersonating-a-client"></a>Rappresentazione di un client

Quando un'applicazione utente richiede dati da oggetti nel sistema tramite un provider WMI, la rappresentazione significa che il provider presenta le credenziali che rappresentano il livello di sicurezza del client anziché l'oggetto del provider. La rappresentazione impedisce a un client di ottenere accesso non autorizzato alle informazioni sul sistema.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Registrazione di un provider per la rappresentazione](#registering-a-provider-for-impersonation)
-   [Impostazione di livelli di rappresentazione in un provider](#setting-impersonation-levels-within-a-provider)
-   [Gestione di livelli di sicurezza in un provider](#maintaining-security-levels-in-a-provider)
-   [Gestione dei messaggi di accesso negato in un provider](#handling-access-denied-messages-in-a-provider)
-   [Segnalazione di istanze parziali](#reporting-partial-instances)
-   [Segnalazione di enumerazioni parziali](#reporting-partial-enumerations)
-   [Debug del codice di accesso negato](#debugging-your-access-denied-code)
-   [Argomenti correlati](#related-topics)

WMI viene in genere eseguito come servizio amministrativo a un livello di sicurezza elevato, usando il contesto di sicurezza LocalServer. L'utilizzo di un servizio amministrativo fornisce a WMI i mezzi per accedere alle informazioni privilegiate. Quando si chiama un provider per informazioni, WMI passa il proprio ID di sicurezza (SID) al provider, consentendo al provider di accedere alle informazioni allo stesso livello di sicurezza elevato.

Durante il processo di avvio dell'applicazione WMI, il sistema operativo Windows fornisce all'applicazione WMI il contesto di sicurezza dell'utente che ha avviato il processo. Il contesto di sicurezza dell'utente è in genere un livello di sicurezza inferiore rispetto a LocalServer, pertanto l'utente potrebbe non disporre delle autorizzazioni necessarie per accedere a tutte le informazioni disponibili in WMI. Quando l'applicazione utente richiede informazioni dinamiche, WMI passa il SID dell'utente al provider corrispondente. Se scritto in modo appropriato, il provider tenta di accedere alle informazioni con il SID dell'utente, anziché il SID del provider.

Affinché il provider rappresenti correttamente l'applicazione client, è necessario che l'applicazione client e il provider soddisfino i criteri seguenti:

-   È necessario che l'applicazione client chiami WMI con un livello di sicurezza della connessione COM di **RPC \_ c \_ Imp level \_ \_ Impersonate** o di **RPC \_ c \_ Imp \_ level \_ delegate**. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).
-   Il provider deve eseguire la registrazione con WMI come provider di rappresentazione. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider per la rappresentazione](#registering-a-provider-for-impersonation).
-   Il provider deve passare al livello di sicurezza dell'applicazione client prima di accedere alle informazioni privilegiate. Per ulteriori informazioni, vedere [impostazione dei livelli di rappresentazione in un provider](#setting-impersonation-levels-within-a-provider).
-   Il provider deve gestire correttamente le condizioni di errore se l'accesso a queste informazioni viene negato. Per ulteriori informazioni, vedere [gestione dei messaggi di accesso negato in un provider](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registrazione di un provider per la rappresentazione

WMI passa il SID di un'applicazione client solo ai provider che hanno eseguito la registrazione come provider di rappresentazione. Per consentire a un provider di eseguire la rappresentazione è necessario modificare il processo di registrazione del provider.

Nella procedura riportata di seguito viene descritto come registrare un provider per la rappresentazione. Nella procedura si presuppone che l'utente abbia già compreso il processo di registrazione. Per ulteriori informazioni sul processo di registrazione, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).

**Per registrare un provider per la rappresentazione**

1.  Impostare la proprietà [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) della classe [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider su 1.

    La proprietà [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) documenta se il provider supporta o meno la rappresentazione. L'impostazione di **ImpersonationLevel** su 0 indica che il provider non rappresenta il client ed esegue tutte le operazioni richieste nello stesso contesto utente di WMI. Se si imposta **ImpersonationLevel** su 1, il provider utilizza chiamate di rappresentazione per verificare le operazioni eseguite per conto del client.

2.  Impostare la proprietà **PerUserInitialization** della stessa classe [**\_ \_ Win32Provider**](--win32provider.md) su **true**.

> [!Note]  
> Se si registra un provider con la proprietà [**\_ \_ Win32Provider**](--win32provider.md) **InitializeAsAdminFirst** impostata su **true**, il provider utilizzerà il token di sicurezza thread a livello di amministrazione solo durante la fase di inizializzazione. Mentre una chiamata a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) non ha esito negativo, il provider usa il contesto di sicurezza di WMI e non del client.

 

Nell'esempio di codice riportato di seguito viene illustrato come registrare un provider per la rappresentazione.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Impostazione di livelli di rappresentazione in un provider

Se si registra un provider con la proprietà della classe [**\_ \_ Win32Provider**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) impostata su 1, WMI chiama il provider per rappresentare diversi client. Per gestire queste chiamate, usare le funzioni com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) nell'implementazione dell'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

La funzione [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) consente a un server di rappresentare il client che ha effettuato la chiamata. Inserendo una chiamata a **CoImpersonateClient** nell'implementazione di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), si consente al provider di impostare il token del thread del provider in modo che corrisponda al token del thread del client e quindi rappresentare il client. Se non si chiama **CoImpersonateClient**, il provider esegue il codice a un livello di sicurezza di amministratore, creando così una potenziale vulnerabilità di sicurezza. Se il provider deve agire temporaneamente come amministratore o eseguire manualmente il controllo dell'accesso, chiamare [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).

A differenza di [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) è una funzione com che gestisce i livelli di rappresentazione del thread. In questo caso, **CoRevertToSelf** modifica di nuovo il livello di rappresentazione nell'impostazione di rappresentazione originale. In generale, il provider è inizialmente un amministratore e si alterna tra **CoImpersonateClient** e **CoRevertToSelf** , a seconda che venga effettuato o meno una chiamata che rappresenta il chiamante o le proprie chiamate. È responsabilità del provider inserire correttamente le chiamate in modo da non esporre un problema di sicurezza all'utente finale. Il provider, ad esempio, deve chiamare solo le funzioni Windows native all'interno della sequenza di codice rappresentata.

> [!Note]  
> Lo scopo di [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) è quello di impostare la sicurezza per un provider. Se si determina che la rappresentazione ha avuto esito negativo, è necessario restituire un codice di completamento appropriato a WMI tramite [**IWbemObjectSink:: sestato**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Per ulteriori informazioni, vedere [gestione dei messaggi di accesso negato in un provider](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Gestione di livelli di sicurezza in un provider

I provider non possono chiamare [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) una sola volta in un'implementazione di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e presuppongono che le credenziali di rappresentazione rimangano valide per la durata del provider. Al contrario, chiamare **CoImpersonateClient** più volte nel corso di un'implementazione di per impedire la modifica delle credenziali da parte di WMI.

La preoccupazione principale per l'impostazione della rappresentazione per un provider è la rientranza. In questo contesto, la rientranza si verifica quando un provider effettua una chiamata a WMI per informazioni e attende fino a quando WMI richiama il provider. In sostanza, il thread di esecuzione lascia il codice del provider, solo per reimmettere il codice in un secondo momento. Il rientro è parte della progettazione di COM e non è in genere un problema. Tuttavia, quando il thread di esecuzione entra in WMI, il thread accetta i livelli di rappresentazione di WMI. Quando il thread torna al provider, è necessario reimpostare i livelli di rappresentazione con un'altra chiamata a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).

Per proteggersi da buchi di sicurezza nel provider, è necessario effettuare chiamate rientranti in WMI solo quando si rappresenta il client. Ovvero, le chiamate a WMI devono essere effettuate dopo la chiamata a [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) e prima di chiamare [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself). Poiché **CoRevertToSelf** fa sì che la rappresentazione sia impostata sul livello utente, WMI è in esecuzione, in genere LocalSystem, le chiamate rientranti a WMI dopo la chiamata di **CoRevertToSelf** potrebbero dare all'utente e a tutti i provider chiamati, molto più funzionalità del necessario.

> [!Note]  
> Se si chiama una funzione di sistema o un altro metodo di interfaccia, non è garantito che il contesto di chiamata venga mantenuto.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Gestione dei messaggi di accesso negato in un provider

La maggior parte dei messaggi di errore di accesso negato viene visualizzata quando un client richiede una classe o informazioni a cui non ha accesso. Se il provider restituisce un messaggio di errore di accesso negato a WMI e WMI lo passa al client, il client può dedurre che esistono le informazioni. In alcune situazioni, può trattarsi di una violazione della sicurezza. Pertanto, il provider non deve propagare il messaggio al client. Al contrario, il set di classi che il provider fornirebbe non dovrebbe essere esposto. Analogamente, un provider di istanze dinamico deve chiamare all'origine dati sottostante per determinare come gestire i messaggi di accesso negato. È responsabilità del provider replicare tale filosofia nell'ambiente WMI. Per ulteriori informazioni, vedere [segnalazione di istanze parziali](#reporting-partial-instances) e [segnalazione di enumerazioni parziali](#reporting-partial-enumerations).

Quando si determina il modo in cui il provider deve gestire i messaggi di accesso negato, è necessario scrivere ed eseguire il debug del codice. Durante il debug, è spesso utile distinguere tra un rifiuto a causa di una rappresentazione bassa e una negazione a causa di un errore nel codice. È possibile utilizzare un semplice test nel codice per determinare la differenza. Per altre informazioni, vedere [debug del codice di accesso negato](#debugging-your-access-denied-code).

## <a name="reporting-partial-instances"></a>Segnalazione di istanze parziali

Un'occorrenza comune di un messaggio di accesso negato è quando WMI non è in grado di fornire tutte le informazioni per riempire un'istanza. Un client, ad esempio, può avere l'autorità di visualizzare un oggetto unità disco rigido, ma potrebbe non avere l'autorità per verificare la quantità di spazio disponibile sull'unità disco rigido. Il provider deve determinare come gestire qualsiasi situazione quando il provider non è in grado di riempire completamente un'istanza con proprietà a causa di una violazione di accesso.

WMI non richiede una singola risposta ai client con accesso parziale a un'istanza di. WMI versione 1. x, invece, consente al provider una delle opzioni seguenti:

-   Interrompere l'intera operazione con **WBEM \_ e \_ accesso \_ negato** e non restituire alcuna istanza.

    Restituisce un oggetto Error insieme a **WBEM \_ E \_ Access \_ Denied** per descrivere il motivo del rifiuto.

-   Restituisce tutte le proprietà disponibili e riempie le proprietà non disponibili con **null**.

> [!Note]  
> Assicurarsi che la restituzione di **WBEM \_ E \_ Access \_ Denied** non crei un problema di sicurezza nell'azienda.

 

## <a name="reporting-partial-enumerations"></a>Segnalazione di enumerazioni parziali

Un'altra occorrenza comune di una violazione di accesso è quando WMI non è in grado di restituire tutte le enumerazioni. Ad esempio, un client può avere accesso per visualizzare tutti gli oggetti computer della rete locale, ma potrebbe non avere accesso per visualizzare gli oggetti computer all'esterno del suo dominio. Il provider deve determinare come gestire una situazione in cui non è possibile completare un'enumerazione a causa di una violazione di accesso.

Come per un provider di istanze, WMI non richiede una singola risposta a un'enumerazione parziale. WMI versione 1. x consente invece a un provider una delle opzioni seguenti:

-   Restituisce **WBEM \_ S \_ nessun \_ errore** per tutte le istanze a cui il provider può accedere.

    Se si usa questa opzione, l'utente non è a conoscenza del fatto che alcune istanze non erano disponibili. Alcuni provider, ad esempio quelli che utilizzano Structured Query Language (SQL) con sicurezza a livello di riga, restituiscono risultati parziali riusciti utilizzando il livello di sicurezza del chiamante per definire il set di risultati.

-   Interrompere l'intera operazione con **WBEM \_ e \_ accesso \_ negato** e non restituire alcuna istanza.

    Il provider può includere facoltativamente un oggetto Error che descrive la situazione al client. Si noti che alcuni provider possono accedere alle origini dati in modo seriale e potrebbero non essere in grado di rilevare i rifiuti fino a legato tramite l'enumerazione.

-   Restituisce tutte le istanze a cui è possibile accedere, ma restituisce anche il codice di stato non di errore. **\_ \_ accesso \_ negato**.

    Il provider deve prendere nota del rifiuto durante l'enumerazione e può continuare a fornire istanze, terminando con il codice di stato non di errore. Il provider può inoltre decidere di terminare l'enumerazione al primo rifiuto. La giustificazione di questa opzione è che provider diversi hanno paradigmi di recupero diversi. È possibile che un provider abbia già recapitato le istanze prima di individuare una violazione di accesso. Alcuni provider possono decidere di continuare a fornire altre istanze e altri potrebbero voler terminare.

A causa della struttura di COM, non è possibile eseguire il marshalling di tutte le informazioni durante un errore, ad eccezione di un oggetto Error. Non è pertanto possibile restituire informazioni e un codice di errore. Se si sceglie di restituire le informazioni, è necessario utilizzare invece un codice di stato non di errore.

## <a name="debugging-your-access-denied-code"></a>Debug del codice di accesso negato

Per alcune applicazioni è possibile utilizzare livelli di rappresentazione inferiori rispetto a quello di **RPC \_ C \_ Imp \_ \_**. In questo caso, la maggior parte delle chiamate di rappresentazione effettuate dal provider per l'applicazione client avrà esito negativo. Per progettare e implementare correttamente un provider, è necessario tenere presente questa idea.

Per impostazione predefinita, l'unico altro livello di rappresentazione che può accedere a un provider è l' **identificazione a livello di RPC \_ C \_ \_ \_ Imp**. Nei casi in cui un'applicazione client utilizza l' **identificazione a livello di RPC \_ C \_ \_ \_ Imp**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) non restituisce un codice di errore. Il provider rappresenta invece il client solo a scopo di identificazione. Pertanto, la maggior parte dei metodi di Windows chiamati dal provider restituirà un messaggio di accesso negato. Si tratta di una procedura innocua, in quanto gli utenti non saranno autorizzati a eseguire alcuna operazione inadeguata. Tuttavia, può essere utile durante lo sviluppo del provider per sapere se il client è stato effettivamente rappresentato o meno.

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

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> </dl>

 

 
