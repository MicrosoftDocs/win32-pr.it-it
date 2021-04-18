---
description: "Un provider di metodi deve implementare IWbemServices come interfaccia primaria. Tuttavia, un provider di metodi puri richiede solo l'implementazione del metodo IWbemServices:: ExecMethodAsync."
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315216"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementazione dell'interfaccia primaria per un provider di metodi

Un provider di metodi deve implementare [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia primaria. Tuttavia, un provider di metodi puri richiede solo l'implementazione del metodo [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Poiché gli altri provider utilizzano [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), l'interfaccia contiene molti metodi irrilevanti per un provider di metodi puri. Il provider di metodi puri deve fornire un'implementazione stub che restituisce \_ il \_ provider WBEM E \_ non \_ idoneo per tutti gli altri metodi **IWbemServices** oltre a [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Tuttavia, molti provider di metodi vengono utilizzati anche come provider di classi o di istanza. Il metodo combinato e i provider di istanze devono supportare più metodi **IWbemServices** .

 

 



