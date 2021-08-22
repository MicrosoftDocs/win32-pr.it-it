---
description: La qualità della protezione, identificata dalla direttiva qop, viene prima specificata dal server nella richiesta di verifica digest e quindi confermata dal client nella risposta alla richiesta di verifica.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualità della protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202acbf319601af74efc35117990f27cc6edff76f27da243453f82bf50984977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920450"
---
# <a name="quality-of-protection"></a>Qualità della protezione

La qualità della protezione, identificata dalla direttiva qop, viene prima specificata dal server nella richiesta di verifica digest e quindi confermata dal client nella risposta alla richiesta di verifica. Se il client richiede una qualità di protezione che il server non supporta, il client deve terminare l'autenticazione.

I valori possibili per la direttiva qop sono descritti nella tabella seguente.



| Valore                   | Descrizione                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| "auth"                  | Solo autenticazione.                                                                                                                         |
| "auth-int"              | Autenticazione e [*controllo dell'integrità*](../secgloss/i-gly.md) tramite firme.                  |
| (solo SASL) "auth-conf" | Controllo di autenticazione, integrità e riservatezza tramite firme e crittografia. Per altre informazioni, vedere [Crittografia.](ciphers.md) |



 

La qualità della protezione è determinata dai flag dei requisiti di contesto passati al Microsoft Digest SSP. Nella tabella seguente sono elencati i flag correlati alla qualità della protezione e il valore risultante della direttiva qop.



| Contrassegno                         | Valore qop               |
|------------------------------|-------------------------|
| *XXX* \_ RISERVATEZZA \_ DELLE RICHIESTE  | "auth-conf" (solo SASL) |
| *XXX* \_ REQ \_ REPLAY \_ DETECT   | "auth-int"              |
| *XXX* \_ REQ \_ SEQUENCE \_ DETECT | "auth-int"              |
| *XXX* \_ INTEGRITÀ \_ REQ        | "auth-int"              |
| (nessuna)                       | "auth"                  |



 

> [!Note]  
> I flag dei requisiti di contesto specificati dalle applicazioni server hanno il prefisso ASC e quelli specificati dai client sono preceduti dal prefisso ISC. Per determinare i valori dei flag usati dall'applicazione, sostituire XXX con uno di questi *prefissi.*

 

Per altre informazioni relative al server, vedere [Generating the Digest Challenge](generating-the-digest-challenge.md).

Per altre informazioni relative al client, vedere [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).

 

 
