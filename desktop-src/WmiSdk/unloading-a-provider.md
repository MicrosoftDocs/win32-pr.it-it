---
description: Al termine dell'operazione WMI, il provider viene scaricato dalla memoria.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Scaricamento di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528465"
---
# <a name="unloading-a-provider"></a>Scaricamento di un provider

Al termine dell'operazione WMI, il provider viene scaricato dalla memoria. Il motivo principale per cui WMI Scarica un provider consiste nel conservare le risorse di sistema. Pertanto, è necessario aggiungere codice che consenta a WMI di scaricare il provider in modo efficiente. Per lo scaricamento di un provider, l'intervallo specificato nel controllo della cache è necessario per due volte.

WMI Scarica un provider in uno dei modi seguenti:

-   Scarica un provider dopo che il provider ha completato le attività fornite.
-   Scarica rapidamente tutti i provider quando l'utente arresta il sistema. Si noti che WMI Scarica i provider in-process quando il servizio WMI viene arrestato dalla riga di comando.

Mentre il primo scenario è più comune, è necessario scrivere il provider per entrambe le possibilità.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Scaricamento di un provider inattivo](#unloading-an-idle-provider)
-   [Accesso al tempo di inattività per un provider](#accessing-the-idle-time-for-a-provider)
-   [Scaricamento di un provider che è anche un client WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Scaricamento di un provider durante la chiusura](#unloading-a-provider-during-shutdown)
-   [Argomenti correlati](#related-topics)

## <a name="unloading-an-idle-provider"></a>Scaricamento di un provider inattivo

Quando Scarica un provider inattivo, WMI esegue le azioni seguenti:

-   Determina se il provider è inattivo.

    WMI utilizza la proprietà **ClearAfter** per determinare per quanto tempo un provider può rimanere inattivo prima di scaricare tale provider. Per ulteriori informazioni, vedere [accesso al tempo di inattività per un provider](#accessing-the-idle-time-for-a-provider).

-   Chiama il metodo di [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) del provider.

    Se il provider è un provider pure, la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) rimuove completamente il provider dalla memoria attiva. Tuttavia, un provider non pure può continuare a essere eseguito dopo il **rilascio** delle chiamate WMI.

## <a name="accessing-the-idle-time-for-a-provider"></a>Accesso al tempo di inattività per un provider

La quantità minima di tempo per cui un provider rimane attivo è determinata dalla proprietà **ClearAfter** . È possibile trovare **ClearAfter** in istanze delle classi derivate dalla classe di sistema WMI [**\_ \_ CacheControl**](--cachecontrol.md) nello \\ spazio dei nomi radice.

Nell'elenco seguente vengono descritte le classi derivate da [**\_ \_ CacheControl**](--cachecontrol.md), che controlla lo scaricamento del provider:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

È possibile modificare la quantità minima di tempo che WMI consente a un provider di rimanere inattivo modificando la proprietà **ClearAfter** nell'istanza del controllo cache per un tipo specifico di provider. Ad esempio, per limitare la quantità di tempo in cui un provider di proprietà può rimanere inattivo, modificare la proprietà **ClearAfter** di un'istanza di [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) nello \\ spazio dei nomi radice.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Scaricamento di un provider che è anche un client WMI

È possibile che il provider debba rimanere un client di WMI dopo aver completato le funzioni del provider chiamate per l'esecuzione. È ad esempio possibile che un provider di push debba eseguire query in WMI. Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md). In questo caso, la proprietà **pure** dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider deve essere impostata su **true**. Se la proprietà **pure** è impostata su **false**, il provider si prepara a eseguire lo scaricamento chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su tutti i punti di interfaccia in attesa quando WMI chiama il metodo release della relativa interfaccia principale. Per ulteriori informazioni, vedere la sezione Osservazioni in [**\_ \_ Win32Provider**](--win32provider.md).

Nella procedura seguente viene descritto come implementare un metodo di rilascio per l'interfaccia principale del provider.

**Per scaricare un provider**

1.  Rilascia tutti i puntatori di interfaccia mantenuti su WMI quando WMI chiama il metodo di [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dell'interfaccia principale del provider.

    In genere, un provider include i puntatori alle interfacce [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) fornite in [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Se la proprietà **pure** nell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) associata è impostata su **false**, il provider può passare al ruolo di applicazione client dopo la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)di WMI. Tuttavia, WMI non è in grado di scaricare un provider che opera come sistema client, aumentando così l'overhead del sistema.

    Un provider con l'impostazione **pure** su **true** esiste solo per le richieste di servizio. Pertanto, questo tipo di provider non può assumere il ruolo di un'applicazione client e WMI può scaricarlo.

## <a name="unloading-a-provider-during-shutdown"></a>Scaricamento di un provider durante la chiusura

In circostanze normali, l'utilizzo delle linee guida nello scaricamento di [un provider che è anche un client WMI](#unloading-a-provider-that-is-also-a-wmi-client) consente a WMI di scaricare il provider in modo corretto. Tuttavia, è possibile che si verifichino situazioni in cui WMI non è in grado di avviare le normali procedure di scaricamento, ad esempio quando l'utente sceglie di arrestare il sistema. Utilizzando un modello di transazione di archiviazione dei dati, oltre all'implementazione di una strategia di pulizia valida, è possibile verificare che il provider sia stato scaricato correttamente.

L'utente può arrestare WMI in qualsiasi momento. In una situazione di questo tipo, WMI non Scarica alcun provider né chiama il punto di ingresso [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) in alcun provider in-process. Inoltre, se un provider in-process si trova al centro di una chiamata al metodo al momento dell'arresto, WMI può eventualmente terminare il thread in esecuzione al centro della chiamata. In questa circostanza, WMI non chiama routine che in genere gestiscono la pulizia, ad esempio un distruttore di oggetti. WMI chiamerà al massimo solo [**DllMain**](/windows/desktop/Dlls/dllmain) .

Quando il sistema operativo arresta WMI, il sistema rilascia automaticamente tutta la memoria allocata a un provider in-process. Il sistema operativo chiude anche la maggior parte delle risorse utilizzate dal provider, ad esempio handle di file, handle di finestra e così via. Per eseguire questa operazione, il provider non deve intraprendere alcuna azione specifica.

Poiché WMI potrebbe arrestarsi durante una chiamata, un provider non deve lasciare le origini dati in uno stato incoerente. Lasciare i dati in uno stato incoerente non è un problema per i provider di sola lettura. Tuttavia, i provider con funzionalità di scrittura potrebbero voler implementare una sorta di modello di transazione per consentire un rollback sicuro dopo un'interruzione improvvisa.

Mentre il sistema operativo può rilasciare alcune risorse di sistema generali, il sistema non rilascia automaticamente tutte le risorse. Ad esempio, il sistema operativo potrebbe non rilasciare un socket o una connessione di database. Al contrario, è possibile che il provider debba eseguire manualmente la pulizia di tali risorse. Per evitare questi problemi, è possibile implementare il provider out-of-process oppure è possibile aggiungere il codice di pulizia.

La soluzione più semplice consiste nell'implementare il provider out-of-process. Un provider out-of-process non viene terminato quando WMI viene arrestato, sebbene WMI rilascerà il provider dopo un timeout COM. I provider per i quali si verificano problemi di affidabilità della pulizia e della terminazione sono più importanti delle prestazioni che potrebbero essere out-of-process.

Se è necessario inserire il codice di pulizia nel provider, sono disponibili due opzioni. Un'unica posizione per eseguire questo tipo di pulizia è [**DllMain**](/windows/desktop/Dlls/dllmain), ovvero la funzione del punto di ingresso della DLL chiamata dal sistema operativo durante lo scaricamento della dll. Il codice di pulitura può essere aggiunto direttamente in **DllMain**, eseguendolo in risposta alla **\_ \_ disconnessione del processo dll**. L'implementazione del codice di pulizia in **DllMain** può essere piuttosto difficile da disporre, soprattutto in ambienti di programmazione come MFC o ATL. Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge base Q148791, "*come specificare DllMain in una DLL regolare MFC".* Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

In alternativa, è anche possibile inserire il codice di pulizia nel distruttore di una classe globale. Per ulteriori informazioni, vedere Scaricamento di un provider. Il sistema operativo Windows non alloca oggetti globali nell'heap. Al contrario, il sistema operativo chiama i distruttori durante lo scaricamento della DLL.

Di seguito è riportata una semplice procedura di pulizia che può rientrare in un oggetto globale per WMI.


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



Esistono diverse restrizioni relative a ciò che è possibile eseguire nel codice di pulizia con entrambi gli approcci. Non è ad esempio possibile accedere ai thread né a qualsiasi dll non collegata in modo implicito. Inoltre, non è possibile effettuare chiamate COM in qualsiasi circostanza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
