---
description: Un messaggio in busta digitale è un messaggio crittografato per un destinatario o un set di destinatari.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Creazione e ricezione di messaggi di dati in busta digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306470"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Creazione e ricezione di messaggi di dati in busta digitale

Un messaggio in busta digitale è un messaggio crittografato per un set di destinatari. Nel processo di inviluppo viene generata una chiave di crittografia della sessione e il messaggio viene crittografato con tale chiave. La chiave di crittografia stessa viene quindi crittografata separatamente per ogni destinatario utilizzando le chiavi pubbliche di ogni certificato del destinatario previsto. Il messaggio in busta digitale è costituito dal messaggio crittografato, dai certificati dei destinatari desiderati e dal set di chiavi crittografate, uno per ogni destinatario. Il messaggio generato è in formato [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.

Le sezioni seguenti illustrano le procedure e gli esempi per le attività dei messaggi in busta:

-   [Codifica dei dati in busta](encoding-enveloped-data.md)
-   [Decodifica dei dati in busta](decoding-enveloped-data.md)
-   [Codice alternativo per la codifica di un messaggio in busta digitale](alternate-code-for-encoding-an-enveloped-message.md)
-   [Esempio di programma C: codifica di un messaggio firmato in busta](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
