---
description: Un puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui viene scritto il byte successivo.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Puntatori a file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226874"
---
# <a name="file-pointers"></a>Puntatori a file

Quando un file viene aperto, Windows associa un *puntatore di file* al flusso predefinito. Questo puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui viene scritto il byte successivo. Ogni volta che un file viene aperto, il sistema posiziona il puntatore del file all'inizio del file, ovvero l'offset zero. Ogni operazione di lettura e scrittura sposta il puntatore del file in base al numero di byte letti e scritti. Se, ad esempio, il puntatore del file si trova all'inizio del file e viene richiesta un'operazione di lettura di 5 byte, il puntatore del file sarà posizionato in corrispondenza dell'offset 5 immediatamente dopo l'operazione di lettura. Poiché ogni byte viene letto o scritto, il sistema sposta in avanti il puntatore del file. Il puntatore del file può essere riposizionato anche chiamando la funzione [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .

Quando il puntatore del file raggiunge la fine di un file e l'applicazione tenta di leggere dal file, non si verifica alcun errore, ma non viene letto alcun byte. Pertanto, la lettura di zero byte senza errori indica che l'applicazione ha raggiunto la fine del file. La scrittura di zero byte non esegue alcuna operazione.

Un'applicazione può troncare o estendere un file tramite la funzione [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) . Questa funzione imposta la fine del file sulla posizione corrente del puntatore del file.

 

 



