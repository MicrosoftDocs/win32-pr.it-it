---
description: Al termine di WMI con un provider, scarica il provider dalla memoria.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Scaricamento di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b831f69ba27ab3e173920cc57e7500ef543bb327a04dc5c04dc8b0b9cef31ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049959"
---
# <a name="unloading-a-provider"></a>Scaricamento di un provider

Al termine di WMI con un provider, scarica il provider dalla memoria. Il motivo principale per cui WMI scarica un provider è risparmiare risorse di sistema. Pertanto, è necessario aggiungere codice che consenta a WMI di scaricare il provider in modo efficiente. Accetta da un punto qualsiasi dall'intervallo specificato nel controllo della cache al doppio dell'intervallo per lo scaricamento di un provider da parte di WMI.

WMI scarica un provider in uno dei modi seguenti:

-   Scaricare un provider dopo che il provider ha completato le attività assegnate.
-   Scaricare rapidamente tutti i provider quando l'utente arresta il sistema. Si noti che WMI scarica i provider in-process quando il servizio WMI viene arrestato dalla riga di comando.

Anche se il primo scenario è più comune, è necessario scrivere il provider per entrambe le possibilità.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Scaricamento di un provider inattivo](#unloading-an-idle-provider)
-   [Accesso al tempo di inattività per un provider](#accessing-the-idle-time-for-a-provider)
-   [Scaricamento di un provider che è anche un client WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Scaricamento di un provider durante l'arresto](#unloading-a-provider-during-shutdown)
-   [Argomenti correlati](#related-topics)

## <a name="unloading-an-idle-provider"></a>Scaricamento di un provider inattivo

WMI esegue le azioni seguenti quando scarica un provider inattivo:

-   Determina se il provider è inattivo.

    WMI usa la **proprietà ClearAfter** per determinare per quanto tempo un provider può rimanere inattivo prima di scaricarlo. Per altre informazioni, vedere [Accesso al tempo di inattività per un provider](#accessing-the-idle-time-for-a-provider).

-   Chiama il [**metodo Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) del provider.

    Se il provider era un provider puro, [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) rimuove completamente il provider dalla memoria attiva. Tuttavia, un provider non di base può continuare a essere eseguito dopo che WMI ha chiamato **Release**.

## <a name="accessing-the-idle-time-for-a-provider"></a>Accesso al tempo di inattività per un provider

La quantità minima di tempo per cui un provider rimane attivo è determinata dalla **proprietà ClearAfter.** È possibile trovare **ClearAfter** nelle istanze di classi derivate dalla classe di sistema WMI [**\_ \_ CacheControl**](--cachecontrol.md) nello spazio \\ dei nomi radice.

L'elenco seguente descrive le classi derivate da [**\_ \_ CacheControl**](--cachecontrol.md), che controlla lo scaricamento del provider:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

È possibile modificare la quantità minima di tempo per cui WMI consente a un provider di rimanere inattivo modificando la proprietà **ClearAfter** nell'istanza del controllo della cache per un tipo specifico di provider. Ad esempio, per limitare il tempo di inattività di un provider di proprietà, è necessario modificare la proprietà **ClearAfter** di un'istanza [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) nello spazio \\ dei nomi radice.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Scaricamento di un provider che è anche un client WMI

Il provider potrebbe dover rimanere un client di WMI dopo aver completato le funzioni del provider che è stato chiamato per eseguire. Ad esempio, un provider push potrebbe dover inviare query a WMI. Per altre informazioni, vedere [Determinazione dello stato push o pull](determining-push-or-pull-status.md). In questo caso, la **proprietà Pure** [**\_ \_ dell'istanza Win32Provider**](--win32provider.md) che rappresenta il provider deve essere impostata su **TRUE.** Se la **proprietà Pure** è impostata su **FALSE,** il provider si prepara allo scaricamento chiamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in sospeso quando WMI chiama il metodo Release della relativa interfaccia primaria. Per altre informazioni, vedere la sezione Osservazioni in [**\_ \_ Win32Provider**](--win32provider.md).

La procedura seguente descrive come implementare un metodo di rilascio per l'interfaccia primaria del provider.

**Per scaricare un provider**

1.  Rilasciare tutti i puntatori a interfaccia contenuti in WMI quando WMI chiama il [**metodo Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dell'interfaccia primaria del provider.

    In genere, un provider contiene puntatori [**alle interfacce IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) fornite in [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Se la **proprietà Pure** nell'istanza [**\_ \_ Win32Provider**](--win32provider.md) associata è impostata su **FALSE,** il provider può passare al ruolo dell'applicazione client dopo che WMI ha chiamato [**Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Tuttavia, WMI non può scaricare un provider che opera come sistema client, con un aumento del sovraccarico del sistema.

    Un provider con **Pure** impostato su **TRUE** esiste solo per le richieste di servizio. Pertanto, questo tipo di provider non può assumere il ruolo di un'applicazione client e WMI può scaricarlo.

## <a name="unloading-a-provider-during-shutdown"></a>Scaricamento di un provider durante l'arresto

In circostanze normali, l'uso delle linee guida in Scaricare un provider che è anche un client WMI consente [a WMI](#unloading-a-provider-that-is-also-a-wmi-client) di scaricare correttamente il provider. Tuttavia, è possibile che wmi non sia in grado di avviare le normali procedure di scaricamento, ad esempio quando l'utente sceglie di arrestare il sistema. Usando un modello di transazione di archiviazione dei dati, oltre a implementare una buona strategia di pulizia, è possibile assicurarsi che il provider venga scaricato correttamente.

L'utente può arrestare WMI in qualsiasi momento. In questo caso, WMI non scarica alcun provider né chiama il punto di ingresso [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) in qualsiasi provider in-process. Inoltre, se un provider in-process si trova nel mezzo di una chiamata al metodo al momento dell'arresto, WMI può terminare il thread in esecuzione nel mezzo della chiamata. In questo caso, WMI non chiama routine che in genere gestiscono la pulizia, ad esempio un distruttore di oggetti. Al massimo, WMI chiamerà [**solo DllMain.**](/windows/desktop/Dlls/dllmain)

Quando il sistema operativo arresta WMI, il sistema rilascia automaticamente tutta la memoria allocata a un provider in-process. Il sistema operativo chiude anche la maggior parte delle risorse utilizzate dal provider, ad esempio handle di file, handle di finestra e così via. Il provider non deve eseguire alcuna azione specifica per eseguire questa operazione.

Poiché WMI può essere arrestato nel corso di una chiamata, un provider non deve lasciare le origini dati in uno stato incoerente. Lasciare i dati in uno stato incoerente non è un problema per i provider di sola lettura. Tuttavia, i provider con funzionalità di scrittura possono voler implementare una sorta di modello di transazione per consentire un rollback sicuro dopo una terminazione improvviso.

Anche se il sistema operativo può rilasciare alcune risorse di sistema generali, il sistema non rilascia automaticamente tutte le risorse. Ad esempio, il sistema operativo potrebbe non rilasciare un socket o una connessione di database. Al contrario, il provider potrebbe dover pulire manualmente tali risorse. Per evitare questi problemi, è possibile implementare il provider out-of-process oppure aggiungere codice di pulizia.

La soluzione più semplice consiste nell'implementare il provider out-of-process. Un provider out-of-process non viene arrestato all'arresto di WMI, anche se WMI rilascerà il provider dopo un timeout COM. I provider per i quali i problemi di affidabilità di pulizia e terminazione sono più importanti delle prestazioni possono essere out-of-process.

Se è necessario inserire il codice di pulizia nel provider, sono disponibili due opzioni. Un posto in cui eseguire questo tipo di pulizia è [**DllMain**](/windows/desktop/Dlls/dllmain), la funzione del punto di ingresso DLL chiamata dal sistema operativo durante lo scaricamento della DLL. Il codice di pulizia può essere aggiunto direttamente in **DllMain,** eseguendolo in risposta a **DLL PROCESS \_ \_ DETACH**. L'implementazione del codice di pulizia in **DllMain** può essere piuttosto difficile da organizzare, soprattutto in ambienti di programmazione come MFC o ATL. Per altre informazioni, vedere l'articolo Microsoft Knowledge Base Q148791, "*How to Provide Your Own DllMain in an MFC Regular DLL "*(Come fornire una dllmain personalizzata in una DLL regolare MFC). " Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

In alternativa, è anche possibile inserire il codice di pulizia nel distruttore di una classe globale. Per altre informazioni, vedere Scaricamento di un provider. Il Windows sistema operativo non alloca oggetti globali nell'heap. Al contrario, il sistema operativo chiama i distruttori durante lo scaricamento della DLL.

Di seguito è riportata una semplice procedura di pulizia che può essere eseguita all'interno di un oggetto globale per WMI.


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



Esistono molte restrizioni sulle operazioni che è possibile eseguire nel codice di pulizia con entrambi gli approcci. Ad esempio, non è possibile accedere in alcun modo ai thread né alle DLL non collegate in modo implicito. Inoltre, non è possibile effettuare chiamate COM in nessun caso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
