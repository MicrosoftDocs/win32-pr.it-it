---
title: Uso Transport-Level sicurezza nel client
description: Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringhe.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- Chiamata di procedura remota RPC, attività, uso della sicurezza a livello di trasporto nel client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee610da50d34711c9ec40f93c29ed08d2bb97ba83c02bc4e8c297b08f859c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010599"
---
# <a name="using-transport-level-security-on-the-client"></a>Uso Transport-Level sicurezza nel client

Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringhe. Queste informazioni QOS vengono fornite come opzione endpoint nell'associazione di stringhe. Il client può specificare il livello di rappresentazione, il rilevamento dinamico o statico e il flag di sola validità.

**Per fornire informazioni sulla qualità del servizio per il server**

1.  Il client chiama [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) per creare le stringhe del componente, incluse le opzioni dell'endpoint, nel contesto corretto di associazione di stringhe.
2.  Il client chiama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere un nuovo handle di associazione e applicare le informazioni sulla qualità del servizio per il client.
3.  Il client esegue chiamate di procedura remota usando l'handle .

Microsoft RPC supporta le Windows di sicurezza solo in [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) e [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Le opzioni di sicurezza per altri trasporti vengono ignorate.

Il client può associare i parametri di sicurezza seguenti all'associazione per il trasporto named pipe [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identificazione, rappresentazione o anonima. Specifica il tipo di sicurezza utilizzato. Il valore predefinito è Rappresentazione.
-   Dinamico o statico. Determina se le informazioni di sicurezza associate a un thread sono una copia delle informazioni di sicurezza create al momento della chiamata di procedura remota (statica) o un puntatore alle informazioni di sicurezza (dinamiche).

    Le informazioni di sicurezza statiche non cambiano. L'impostazione dinamica riflette le impostazioni di sicurezza correnti, incluse le modifiche apportate dopo la chiamata di procedura remota. Per [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np), l'impostazione predefinita per le connessioni named pipe remote è statica, per le connessioni named pipe locali il valore predefinito è dinamico.

-   **TRUE** o **FALSE.** Specifica il valore del flag di sola validità. Il valore **TRUE** indica che solo i privilegi del token impostati su on al momento della chiamata sono effettivi. Il valore **FALSE** indica che tutti i privilegi sono disponibili e che l'applicazione può modificarli.

Qualsiasi combinazione di queste impostazioni può essere assegnata all'associazione, come illustrato nell'esempio seguente:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

Le impostazioni predefinite dei parametri di sicurezza variano in base al protocollo di trasporto.

Per altre informazioni sulla sintassi delle opzioni dell'endpoint, vedere [endpoint](/windows/desktop/Midl/endpoint).

 

 