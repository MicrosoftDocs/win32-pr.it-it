---
description: In altre circostanze è possibile completare un'operazione di lettura o scrittura con un numero di caratteri inferiore a quello richiesto, anche se non si è verificato un timeout.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Errori di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483285"
---
# <a name="communications-errors"></a>Errori di comunicazione

In altre circostanze è possibile completare un'operazione di lettura o scrittura con un numero di caratteri inferiore a quello richiesto, anche se non si è verificato un timeout. Ecco alcuni esempi:

-   Alcuni driver supportano l'uso di caratteri speciali, che completano immediatamente un'operazione di lettura con solo i caratteri che sono stati letti fino al momento in cui vengono ricevuti.
-   La funzione [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) può essere chiamata per terminare in modo anomalo le operazioni di lettura o scrittura in sospeso. Questa funzione può anche eliminare il contenuto dei buffer di output o di input o entrambi.
-   Se si verifica un errore di comunicazione durante un'operazione di lettura o scrittura, tutte le operazioni di I/O sulla risorsa di comunicazione vengono terminate. Condizioni di interruzioni, errori di parità o errori di framing sono esempi di tali errori. Quando si verifica un errore, è necessario che il processo chiami la funzione [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) per cancellare il flag di errore prima di poter avviare ulteriori operazioni di I/O. **ClearCommError** segnala l'errore specifico che si è verificato e lo stato corrente del dispositivo.

 

 



