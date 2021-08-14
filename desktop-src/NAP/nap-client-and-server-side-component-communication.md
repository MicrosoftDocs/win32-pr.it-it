---
title: Comunicazione tra client e componenti lato server di Protezione accesso alla rete
description: Comunicazione tra client e componenti lato server di Protezione accesso alla rete
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3c390aa8bdc8cc80eec8834dd1c250d523737d63963b4b9370877ffa46329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799078"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicazione tra client e componenti lato server di Protezione accesso alla rete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il componente Agente Protezione accesso alla rete può comunicare con il componente Server di amministrazione protezione accesso alla rete tramite il processo seguente:

1.  L'agente protezione accesso alla rete passa SSoH all'ec di Protezione accesso alla rete.
2.  L'ec di Protezione accesso alla rete passa SSoH al sistema ES di Protezione accesso alla rete.
3.  Il servizio Protezione accesso alla rete passa SSoH al servizio Server dei criteri di rete.
4.  Il servizio Server dei criteri di rete passa SSoH al server di amministrazione di Protezione accesso alla rete.

Un'sha può comunicare con il valore SHV corrispondente tramite il processo seguente:

1.  L'SHA passa il soH all'agente protezione accesso alla rete.
2.  L'agente di Protezione accesso alla rete passa il file SoH, contenuto all'interno di SSoH, all'ec di Protezione accesso alla rete.
3.  L'entità di protezione accesso alla rete passa il soH al servizio Protezione accesso alla rete.
4.  Il servizio Protezione accesso alla rete passa il soH al server di amministrazione di Protezione accesso alla rete.
5.  Il server di amministrazione di Protezione accesso alla rete passa il soh all'istanza shv.

La figura seguente mostra il processo di comunicazione tra i componenti client di Protezione accesso alla rete e i componenti lato server di Protezione accesso alla rete.

![architettura della comunicazione client-server nella piattaforma nap](images/nap-client-to-server-comm.png)

Il server di amministrazione di Protezione accesso alla rete può comunicare con l'agente protezione accesso alla rete tramite il processo seguente:

1.  Il server di amministrazione di Protezione accesso alla rete passa i soHR al servizio Server dei criteri di rete.
2.  Il servizio Server dei criteri di rete passa SSoHR al servizio Protezione accesso alla rete.
3.  L'ES di Protezione accesso alla rete passa SSoHR all'ec di Protezione accesso alla rete.
4.  Nap EC passa SSoHR all'agente protezione accesso alla rete.

ShV può comunicare con l'SHA corrispondente tramite il processo seguente:

1.  ShV passa il proprio SoHR al server di amministrazione di Protezione accesso alla rete.
2.  Il server di amministrazione di Protezione accesso alla rete passa soHR al servizio Server dei criteri di rete.
3.  Il servizio Server dei criteri di rete passa il soHR, contenuto all'interno di SSoHR, al sistema ES di Protezione accesso alla rete.
4.  L'ES di Protezione accesso alla rete passa la sohr all'ec di Protezione accesso alla rete.
5.  Nap EC passa il SoHR all'agente protezione accesso alla rete.
6.  L'agente protezione accesso alla rete passa SoHR all'SHA.

La figura seguente mostra il processo di comunicazione tra i componenti lato server di Protezione accesso alla rete e i componenti client di Protezione accesso alla rete.

![architettura della comunicazione da server a client nella piattaforma nap](images/nap-server-to-client-comm.png)

 

 




