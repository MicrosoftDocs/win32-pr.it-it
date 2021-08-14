---
title: Composizione del nome SPN di un servizio da parte dei client
description: Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Modalità di composizione dell'ad SPN di un servizio da parte dei client
- nome dell'entità servizio AD , come i client compongono il nome SPN di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188186"
---
# <a name="how-clients-compose-a-services-spn"></a>Composizione del nome SPN di un servizio da parte dei client

Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi. L'applicazione client può usare la [**funzione DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) per comporre un nome SPN. Il client specifica i componenti del nome SPN usando dati noti o dati recuperati da origini diverse dal servizio stesso.

Il formato di un nome SPN è come illustrato nel formato seguente:


```C++
<service class>/<host>:<port>/<service name>
```



In questo formato sono necessari " &lt; classe di servizio " e " host &gt; &lt; &gt; ". " &lt; port " e " service name " &gt; &lt; &gt; facoltativo.

In genere, il client riconosce la parte " classe del servizio " del nome e riconosce quali componenti &lt; &gt; facoltativi includere nel nome SPN. Il client può recuperare i componenti del nome SPN da origini quali un punto di connessione del servizio (SCP) o l'input dell'utente. Ad esempio, il client può leggere **l'attributo serviceDNSName** del punto di connessione del servizio per ottenere il componente " &lt; host &gt; ". **L'attributo serviceDNSName** contiene il nome DNS del server in cui è in esecuzione l'istanza del servizio o il nome DNS dei record SRV contenenti i dati host per le repliche del servizio. Il componente " service name ", usato solo per i servizi replicabili, può essere il nome distinto del SCP del servizio, il nome DNS del dominio servito dal servizio o il nome DNS dei record SRV o &lt; &gt; MX.

Per altre informazioni e un esempio di codice usato per comporre un nome SPN per un servizio, vedere How [a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Per altre informazioni e una descrizione dei componenti SPN, vedere [Formati dei nomi SPN univoci.](name-formats-for-unique-spns.md)

 

 




