---
description: Un Message Authentication Code (MAC) viene usato per rilevare la manomissione e la falsificazione dei messaggi.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Codici di autenticazione dei messaggi in Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db81efbaa71dc94094e5efb14d11dde600798cc8f58855a3a3ae116a624b679f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786983"
---
# <a name="message-authentication-codes-in-schannel"></a>Codici di autenticazione dei messaggi in Schannel

Un [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) viene usato per rilevare la manomissione e la falsificazione dei messaggi. Il mittente di un messaggio crea un MAC crittografando un [*hash*](../secgloss/h-gly.md) unidirede del corpo del messaggio usando una [*chiave di*](../secgloss/s-gly.md) sessione condivisa dal mittente e dal destinatario. Il MAC viene aggiunto al messaggio inviato al destinatario. Il destinatario del messaggio genera nuovamente il MAC, usando la chiave di sessione condivisa e il corpo del messaggio, e confronta il MAC generato con il MAC ricevuto dal mittente. Se i due sono identici, il mittente deve avere la chiave di sessione condivisa e il messaggio non è stato modificato in transito.

Nei protocolli Schannel, l'algoritmo usato per generare il MAC è determinato dalla [suite di](cipher-suites-in-schannel.md) crittografia in uso dal mittente e dal destinatario.

 

 
