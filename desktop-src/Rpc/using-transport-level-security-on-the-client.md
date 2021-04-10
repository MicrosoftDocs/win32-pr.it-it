---
title: Utilizzo di Transport-Level sicurezza sul client
description: Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringa.
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- RPC (Remote Procedure Call), attività, uso della sicurezza a livello di trasporto nel client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963379"
---
# <a name="using-transport-level-security-on-the-client"></a>Utilizzo di Transport-Level sicurezza sul client

Il client specifica il modo in cui il server rappresenta il client quando il client stabilisce l'associazione di stringa. Queste informazioni QOS vengono fornite come opzione endpoint nell'associazione di stringa. Il client può specificare il livello di rappresentazione, il rilevamento statico o dinamico e il flag solo valido.

**Per fornire informazioni sulla qualità del servizio per il server**

1.  Il client chiama [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) per creare le stringhe dei componenti, incluse le opzioni dell'endpoint, nel contesto di associazione stringa corretto.
2.  Il client chiama [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere un nuovo handle di associazione e per applicare le informazioni di qualità del servizio per il client.
3.  Il client effettua chiamate a procedure remote usando l'handle.

Microsoft RPC supporta le funzionalità di sicurezza di Windows solo in [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) e [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Le opzioni di sicurezza per gli altri trasporti vengono ignorate.

Il client può associare i seguenti parametri di sicurezza al binding per il trasporto named pipe [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) o [**ncalrpc**](/windows/desktop/Midl/ncalrpc):

-   Identificazione, rappresentazione o anonima. Specifica il tipo di sicurezza utilizzato. Il valore predefinito è rappresentazione.
-   Statico o dinamico. Determina se le informazioni di sicurezza associate a un thread sono una copia delle informazioni di sicurezza create nel momento in cui viene eseguita la chiamata di procedura remota (statica) o un puntatore alle informazioni di sicurezza (dinamico).

    Le informazioni di sicurezza statiche non cambiano. L'impostazione dinamica riflette le impostazioni di sicurezza correnti, comprese le modifiche apportate dopo la chiamata di procedura remota. Per [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), il valore predefinito per le connessioni named pipe remote è statico, per le connessioni named pipe locali il valore predefinito è Dynamic.

-   **True** o **false**. Specifica il valore del flag solo valido. Il valore **true** indica che solo i privilegi di token impostati su on al momento della chiamata sono validi. Il valore **false** indica che tutti i privilegi sono disponibili e che l'applicazione può modificarli.

Qualsiasi combinazione di queste impostazioni può essere assegnata all'associazione, come illustrato nell'esempio seguente:

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

Le impostazioni predefinite dei parametri di sicurezza variano in base al protocollo di trasporto.

Per ulteriori informazioni sulla sintassi delle opzioni dell'endpoint, vedere [endpoint](/windows/desktop/Midl/endpoint).

 

 