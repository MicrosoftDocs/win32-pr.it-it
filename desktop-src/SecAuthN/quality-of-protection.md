---
description: La qualità della protezione, identificata dalla direttiva qop, viene innanzitutto specificata dal server nella richiesta digest e quindi confermata dal client nella risposta alla richiesta di verifica.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualità della protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058070"
---
# <a name="quality-of-protection"></a>Qualità della protezione

La qualità della protezione, identificata dalla direttiva qop, viene innanzitutto specificata dal server nella richiesta digest e quindi confermata dal client nella risposta alla richiesta di verifica. Se il client richiede una qualità di protezione non supportata dal server, il client deve terminare l'autenticazione.

I valori possibili per la direttiva qop sono descritti nella tabella seguente.



| Valore                   | Descrizione                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| autenticazione                  | Solo autenticazione.                                                                                                                         |
| "auth-int"              | Autenticazione e controllo dell' [*integrità*](../secgloss/i-gly.md) mediante le firme.                  |
| (Solo SASL) "auth-conf" | Autenticazione, verifica dell'integrità e della riservatezza mediante le firme e la crittografia. Per ulteriori informazioni, vedere [crittografie](ciphers.md). |



 

La qualità della protezione è determinata dai flag dei requisiti di contesto passati al SSP Microsoft Digest. Nella tabella seguente sono elencati i flag relativi alla qualità della protezione e il valore risultante della direttiva qop.



| Contrassegno                         | valore qop               |
|------------------------------|-------------------------|
| *Xxx* \_ \_riservatezza richieste  | "auth-conf" (solo SASL) |
| *Xxx* \_ \_rilevamento riproduzione req \_   | "auth-int"              |
| *Xxx* \_ \_rilevamento sequenza \_ req | "auth-int"              |
| *Xxx* \_ \_integrità req        | "auth-int"              |
| (nessuna)                       | autenticazione                  |



 

> [!Note]  
> I flag del requisito di contesto specificati dalle applicazioni server hanno un prefisso ASC e quelli specificati dai client sono preceduti da ISC. Per determinare i valori dei flag usati dall'applicazione, sostituire uno di questi prefissi per *xxx*.

 

Per informazioni aggiuntive relative al server, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).

Per informazioni aggiuntive relative al client, vedere [generazione della risposta alla richiesta digest](generating-the-digest-challenge-response.md).

 

 
