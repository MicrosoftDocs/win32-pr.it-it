---
description: Un messaggio in busta è un messaggio crittografato per un destinatario o un set di destinatari.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Creazione e ricezione di messaggi di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768906"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Creazione e ricezione di messaggi di dati in busta

Un messaggio in busta è un messaggio crittografato per un set di destinatari. Nel processo di ambiente viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave. La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario usando le chiavi pubbliche del certificato di ogni destinatario previsto. Il messaggio in busta è costituito dal messaggio crittografato, dai certificati dei destinatari previsti e dal set di chiavi crittografate, uno per ogni destinatario. Il messaggio generato è in [*formato PKCS \# 7*](../secgloss/p-gly.md)/CMS.

Le sezioni seguenti illustrano procedure ed esempi per le attività dei messaggi in busta:

-   [Codifica dei dati in busta](encoding-enveloped-data.md)
-   [Decodifica dei dati in busta](decoding-enveloped-data.md)
-   [Codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md)
-   [Programma C di esempio: codifica di un messaggio in busta, firmato](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
