---
description: Le funzioni di messaggio di basso livello codificano i dati per la trasmissione e la decodifica dei dati ricevuti. Anche le funzioni di messaggio di basso livello decrittografano e verificano le firme dei messaggi ricevuti.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Funzioni di messaggio di basso livello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752130"
---
# <a name="low-level-message-functions"></a>Funzioni di messaggio di basso livello

Le [*funzioni di messaggio di basso livello*](../secgloss/l-gly.md) codificano i dati per la trasmissione e la decodifica dei dati ricevuti. Anche le funzioni di messaggio di basso livello decrittografano e verificano le firme dei messaggi ricevuti.

Quando un messaggio viene aperto utilizzando una funzione di apertura dei messaggi di basso livello, rimane aperto e disponibile (mantiene il proprio [*stato*](../secgloss/s-gly.md)) finché non viene chiuso. In questo modo è possibile costruire un messaggio a fasi usando più chiamate alla funzione [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .

L'utilizzo di funzioni di messaggio di basso livello richiede più chiamate di funzione rispetto all'utilizzo di funzioni di messaggio semplificate (vedere [messaggi semplificati](simplified-messages.md)). Se vengono usate le funzioni di messaggio semplificate, il lavoro viene eseguito all'interno delle funzioni dell'API.

L'utilizzo di funzioni di messaggio di basso livello implica il lavoro aggiuntivo di effettuare chiamate ad altre funzioni di crittografia o certificati. Ad esempio, è possibile che i dati delle chiamate alle funzioni di certificato siano necessari per inizializzare le strutture utilizzate dalle funzioni di messaggio di basso livello. Le funzioni di messaggio semplificate inizializzano molte di queste strutture internamente.

Nella tabella seguente sono elencate le sezioni con le descrizioni delle procedure e gli esempi di codice C dell'utilizzo delle funzioni di messaggio di basso livello.



| Sezione                                                                               | Contenuto                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Funzioni di messaggio di basso livello](cryptography-functions.md) | Elenca le funzioni di messaggio di basso livello.             |
| [Firma dei dati](signing-data.md)                                                      | Descrive le attività necessarie per la firma dei dati.             |
| [Codifica dei dati in busta](encoding-enveloped-data.md)                                | Descrive le attività necessarie per codificare i dati in busta. |
| [Decodifica dei dati in busta](decoding-enveloped-data.md)                                | Descrive le attività necessarie per decodificare i dati in busta. |



 

 

 
