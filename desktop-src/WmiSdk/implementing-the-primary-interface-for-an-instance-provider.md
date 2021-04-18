---
title: Implementazione di un'interfaccia primaria del provider di istanze
description: Un provider di istanze usa i metodi asincroni di IWbemServices come interfaccia principale di WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315212"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implementazione di un'interfaccia primaria del provider di istanze

Un provider di istanze usa i metodi asincroni di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia principale di WMI. Implementando solo i metodi che soddisfano le esigenze del provider di istanze, è possibile ridurre la quantità di risorse di cui si dedica la codifica. Tuttavia, implementando metodi riservati per altri tipi di provider, è possibile ridurre il numero di provider scritti.

Poiché è usato anche da applicazioni e provider per richiedere servizi di WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contiene molti metodi irrilevanti per un provider di istanze. Nella tabella seguente sono elencati i metodi **IWbemServices** che è possibile implementare per un provider di istanze.



| Metodo                                                                   | Funzionalità          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Recupero        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modifica     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Eliminazione         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Enumerazione      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Elaborazione di query |



 

Per i metodi che non vengono usati, il provider può fornire un'implementazione stub che restituisce **il \_ provider WBEM E che \_ non è \_ \_ in grado** di supportare. Sono inclusi tutti i metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) non elencati nella tabella precedente.

Un singolo provider può agire simultaneamente come provider di classi, istanze e metodi mediante la registrazione e l'implementazione appropriate di tutti i metodi pertinenti. Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di metodi](writing-a-method-provider.md).

 

 



