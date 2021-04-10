---
title: Composizione del nome SPN di un servizio da parte dei client
description: Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Composizione del nome SPN di un servizio da parte dei client
- nome dell'entità servizio AD, modo in cui i client costituiscono il nome SPN di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955139"
---
# <a name="how-clients-compose-a-services-spn"></a>Composizione del nome SPN di un servizio da parte dei client

Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi. L'applicazione client può usare la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) per comporre un nome SPN. Il client specifica i componenti del nome SPN utilizzando dati noti o dati recuperati da origini diverse dal servizio stesso.

Il formato di un nome SPN è come illustrato nel formato seguente:


```C++
<service class>/<host>:<port>/<service name>
```



In questo formato &lt; sono necessari "Service Class &gt; " e " &lt; host &gt; ". " &lt; Port &gt; " e " &lt; Service Name &gt; " facoltativi.

In genere, il client riconosce la &lt; parte "classe &gt; di servizio" del nome e riconosce quale dei componenti facoltativi includere nell'SPN. Il client può recuperare i componenti del nome SPN dalle origini, ad esempio un punto di connessione del servizio (SCP) o l'input dell'utente. Ad esempio, il client può leggere l'attributo **serviceDNSName** del SCP di un servizio per ottenere il &lt; componente "host &gt; ". L'attributo **serviceDNSName** contiene il nome DNS del server in cui è in esecuzione l'istanza del servizio o il nome DNS dei record SRV contenenti i dati host per le repliche del servizio. Il &lt; componente "nome servizio &gt; ", usato solo per i servizi replicabili, può essere il nome distinto del SCP del servizio, il nome DNS del dominio servito dal servizio o il nome DNS dei record SRV o MX.

Per ulteriori informazioni e un esempio di codice utilizzato per comporre un nome SPN per un servizio, vedere [come un client autentica un servizio Windows Sockets basato su SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Per ulteriori informazioni e una descrizione dei componenti SPN, vedere [formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).

 

 




