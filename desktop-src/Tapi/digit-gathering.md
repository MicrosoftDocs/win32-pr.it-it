---
description: Oltre ad abilitare il monitoraggio delle cifre e ricevere una notifica delle cifre una alla volta, un'applicazione può anche richiedere che vengano raccolte più cifre in un buffer.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Raccolta cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309961"
---
# <a name="digit-gathering"></a>Raccolta cifre

Oltre ad abilitare il monitoraggio delle cifre e ricevere una notifica delle cifre una alla volta, un'applicazione può anche richiedere che vengano raccolte più cifre in un buffer. Solo quando il buffer è pieno o quando viene soddisfatta una determinata condizione di terminazione, l'applicazione riceve una notifica. La raccolta di cifre è utile per le funzioni, ad esempio la raccolta dei numeri di carta di credito. Viene eseguita quando un'applicazione chiama [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specificando un buffer da riempire con le cifre. La raccolta di cifre termina quando viene soddisfatta una delle condizioni seguenti:

-   Il numero di cifre richiesto è stato raccolto.
-   È stata rilevata una o più cifre di terminazione. Le cifre di terminazione vengono specificate per [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)e la cifra di chiusura viene inserita anche nel buffer.
-   Uno dei due timeout scade. I timeout sono un timeout della prima cifra, che specifica la durata massima prima che la prima cifra debba essere raccolta e un timeout tra cifre, che specifica la durata massima tra le cifre successive.
-   La raccolta di cifre viene annullata in modo esplicito da [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) di nuovo con un altro set di parametri per avviare una nuova richiesta di raccolta o usando un parametro di buffer a cifre **null** da annullare.

Quando la raccolta di cifre termina per qualsiasi motivo, viene inviato un messaggio di [**riga \_ GATHERDIGITS**](line-gatherdigits.md) all'applicazione che ha richiesto la raccolta delle cifre. In una chiamata in qualsiasi momento, in tutte le applicazioni proprietarie della chiamata, può essere in attesa una sola richiesta di raccolta con una sola cifra.

La raccolta di cifre e il monitoraggio delle cifre possono essere abilitati nella stessa chiamata nello stesso momento. In tal caso, l'applicazione riceverà un messaggio di [**riga \_ MONITORDIGITS**](line-monitordigits.md) per ogni cifra rilevata e un messaggio di riga separato \_ GATHERDIGITS quando il buffer viene restituito.

 

 



