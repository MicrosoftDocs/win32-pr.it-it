---
title: Comunicazione tra client NAP e componenti lato server
description: Comunicazione tra client NAP e componenti lato server
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396679"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicazione tra client NAP e componenti lato server

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il componente agente NAP è in grado di comunicare con il componente server di amministrazione NAP tramite il processo seguente:

1.  L'agente NAP passa il SSoH di protezione accesso alla rete EC.
2.  NAP EC passa il SSoH di protezione accesso alla rete.
3.  NAP ES passa il SSoH al servizio Server dei criteri di rete (NPS).
4.  Il servizio NPS passa il SSoH al server di amministrazione NAP.

Un SHA può comunicare con l'integrità di sistema corrispondente tramite il processo seguente:

1.  SHA passa il rapporto di integrità all'agente NAP.
2.  L'agente NAP passa il rapporto di integrità, contenuto all'interno di SSoH, alla rete di protezione accesso alla rete (EC).
3.  La protezione accesso alla rete EC passa il rapporto di integrità al NAP.
4.  NAP ES passa il rapporto di integrità al server di amministrazione NAP.
5.  Il server di amministrazione NAP passa il rapporto di integrità al servizio di convalida dell'integrità.

Nella figura seguente viene illustrato il processo di comunicazione tra i componenti client NAP e i componenti lato server di NAP.

![architettura della comunicazione da client a server nella piattaforma NAP](images/nap-client-to-server-comm.png)

Il server di amministrazione NAP è in grado di comunicare con l'agente NAP tramite il processo seguente:

1.  Il server di amministrazione NAP passa il SoHRs al servizio Server dei criteri di rete.
2.  Il servizio NPS passa il risposta al rapporto di protezione accesso alla rete.
3.  NAP ES passa il risposta al rapporto di protezione accesso alla rete EC.
4.  Il risposta al rapporto di protezione accesso alla rete EC passa l'agente protezione accesso alla rete.

Il servizio di convalida dell'integrità di sistema può comunicare con l'SHA corrispondente tramite il processo seguente:

1.  Il servizio di convalida dell'integrità di sistema passa il relativo SoHR al server di amministrazione NAP.
2.  Il server di amministrazione NAP passa il SoHR al servizio Server dei criteri di rete.
3.  Il servizio Server dei criteri di rete passa il SoHR, contenuto all'interno di risposta al rapporto, all'ES NAP.
4.  NAP ES passa il SoHR di protezione accesso alla rete EC.
5.  Il SoHR di protezione accesso alla rete EC passa l'agente protezione accesso alla rete.
6.  L'agente NAP passa il SoHR all'SHA.

Nella figura seguente viene illustrato il processo di comunicazione tra i componenti lato server di NAP e i componenti client di protezione accesso alla rete.

![architettura della comunicazione da server a client nella piattaforma NAP](images/nap-server-to-client-comm.png)

 

 




