---
description: Un puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui ricevere il byte successivo scritto.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Puntatori ai file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfe744f341e111e7956bda85401c5b87e063718309f675c33ff551918756239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997032"
---
# <a name="file-pointers"></a>Puntatori ai file

Quando un file viene aperto, Windows un puntatore *di file* al flusso predefinito. Questo puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui ricevere il byte successivo scritto. Ogni volta che un file viene aperto, il sistema posiziona il puntatore del file all'inizio del file, che è l'offset zero. Ogni operazione di lettura e scrittura fa avanzare il puntatore del file in base al numero di byte letti e scritti. Ad esempio, se il puntatore del file si trova all'inizio del file ed è richiesta un'operazione di lettura di 5 byte, il puntatore del file si trova in corrispondenza dell'offset 5 immediatamente dopo l'operazione di lettura. Quando ogni byte viene letto o scritto, il sistema fa avanzare il puntatore del file. Il puntatore del file può anche essere riposizionato chiamando la [**funzione SetFilePointer.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)

Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non vengono letti byte. Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file. La scrittura di zero byte non esegue alcuna operazione.

Un'applicazione può troncare o estendere un file usando la [**funzione SetEndOfFile.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) Questa funzione imposta la fine del file sulla posizione corrente del puntatore del file.

 

 



