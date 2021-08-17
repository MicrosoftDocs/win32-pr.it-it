---
description: Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider ad alte prestazioni come server in-process.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia High-Performance dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108622"
---
# <a name="implementing-the-high-performance-interface"></a>Implementazione dell'interfaccia High-Performance dati

Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider ad alte prestazioni come server in-process. Inoltre, è necessario implementare i metodi del provider ad alte prestazioni nelle interfacce [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

È consigliabile implementare un provider a prestazioni elevate come server in-process. Una funzionalità da tenere presente quando si implementa la sicurezza di un server in-process è il modo in cui il provider identifica la propria posizione. Quando viene caricato in-process in WMI, WMI crea un'istanza del provider usando un CLSID. Quando viene caricata in un processo in un'applicazione client, l'applicazione client crea un'istanza del provider con la **proprietà ClientLoadableCLSID.** Fornendo valori diversi a un CLSID e **a ClientLoadableCLSID**, si consente al provider di determinare se è caricato in-process in WMI o in un'applicazione client. Se si trova in un processo WMI, il provider deve eseguire qualsiasi rappresentazione client necessaria usando **ClientLoadableCLSID**. Se si trova in un processo client, il provider eredita il token di accesso del thread su cui viene chiamato. Per altre informazioni sull'implementazione di un server in-process, vedere la [sezione COM](https://msdn.microsoft.com/library/aa139695.aspx) di MSDN.

Come server in-process, un provider a prestazioni elevate usa un oggetto di aggiornamento per mantenere aggiornati i dati per il client remoto. Nella tabella seguente sono elencati i metodi che è necessario implementare per un provider a prestazioni elevate.



| Metodo                                                                                              | Funzionalità                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Query                                           |
| [**IWbemHiPerfProvider::GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recupero di oggetti                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Crea un aggiornamento                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Crea un oggetto istanza aggiornabile             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Crea un enumeratore aggiornabile                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Arresta l'aggiornamento di un oggetto enumeratore o istanza |
| [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Crea un aggiornamento                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



