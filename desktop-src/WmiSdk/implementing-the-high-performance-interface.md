---
description: Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider a prestazioni elevate come server in-process.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315217"
---
# <a name="implementing-the-high-performance-interface"></a>Implementazione dell'interfaccia High-Performance

Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider a prestazioni elevate come server in-process. Inoltre, è necessario implementare i metodi del provider a prestazioni elevate nelle interfacce [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .

È necessario implementare un provider a prestazioni elevate come server in-process. Una funzionalità da tenere presente quando si implementa la sicurezza di un server in-process è il modo in cui il provider identifica il proprio percorso. Quando viene caricato in-process in WMI, WMI crea un'istanza del provider utilizzando un CLSID. Quando viene caricato in un processo in un'applicazione client, l'applicazione client crea un'istanza del provider con la proprietà **ClientLoadableCLSID** . Se si assegnano valori diversi a un CLSID e a **ClientLoadableCLSID**, si consente al provider di determinare se viene caricato in-process in WMI o in un'applicazione client. Se si trova in un processo WMI, il provider deve eseguire la rappresentazione client necessaria usando **ClientLoadableCLSID**. Se si trova in un processo client, il provider eredita il token di accesso del thread su cui è stato chiamato. Per ulteriori informazioni sull'implementazione di un server in-process, vedere la [sezione com](https://msdn.microsoft.com/library/aa139695.aspx) di MSDN.

Come server in-process, un provider a prestazioni elevate utilizza un oggetto di aggiornamento per garantire la presenza di dati correnti per il client remoto. Nella tabella seguente sono elencati i metodi che è necessario implementare per un provider a prestazioni elevate.



| Metodo                                                                                              | Funzionalità                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Query                                           |
| [**IWbemHiPerfProvider:: GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recupero di oggetti                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Consente di creare un aggiornamento                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Crea un oggetto istanza aggiornabile             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Crea un enumeratore aggiornabile                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Interrompe l'aggiornamento di un oggetto enumeratore o istanza |
| [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Consente di creare un aggiornamento                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



