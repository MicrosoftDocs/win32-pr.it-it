---
description: Il provider di visualizzazione è un'istanza e un provider di metodi che creano nuove classi basate su istanze di altre classi.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Visualizza provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883506"
---
# <a name="view-provider"></a>Visualizza provider

Il provider di visualizzazione è un'istanza e un provider di metodi che creano nuove classi basate su istanze di altre classi. È possibile utilizzare il provider di visualizzazione per eseguire proprietà da classi di origine diverse, spazi dei nomi diversi o computer diversi e combinare le proprietà come una singola classe.

Come provider di istanze e di metodi, il provider di visualizzazione supporta l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard e i metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) seguenti:

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Per ulteriori informazioni sui qualificatori utilizzati per definire le classi del provider di visualizzazione, vedere [qualificatori specifici del provider di visualizzazione](qualifiers-specific-to-the-view-provider.md).

Per ulteriori informazioni sulle visualizzazioni, vedere [collegamento di classi](linking-classes-together.md).

Sulle piattaforme a 64 bit sono disponibili due versioni del provider di visualizzazione. Per altre informazioni, vedere [ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md).

Il provider di visualizzazione viene implementato in ViewProv.dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 



