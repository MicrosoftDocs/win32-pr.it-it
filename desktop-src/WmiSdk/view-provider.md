---
description: Il provider View è un provider di istanze e di metodi che crea nuove classi basate su istanze di altre classi.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Provider di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec84f3a22a777da2212dcfe918f4294495ade54191cd4d37e17f2ac32c2f5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553264"
---
# <a name="view-provider"></a>Provider di visualizzazione

Il provider View è un provider di istanze e di metodi che crea nuove classi basate su istanze di altre classi. È possibile usare il provider View per ottenere proprietà da classi di origine diverse, spazi dei nomi diversi o computer diversi e combinare le proprietà come una singola classe.

Come provider di istanze e metodi, il provider View supporta [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard e i metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) seguenti:

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Per altre informazioni sui qualificatori utilizzati per definire le classi del provider view, vedere [Qualificatori specifici del provider di visualizzazione.](qualifiers-specific-to-the-view-provider.md)

Per altre informazioni sulle visualizzazioni, vedere [Collegamento di classi tra loro.](linking-classes-together.md)

Nelle piattaforme a 64 bit sono disponibili due versioni del provider View. Per altre informazioni, vedere [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).

Il provider View viene implementato in ViewProv.dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 



