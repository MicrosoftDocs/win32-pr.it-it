---
title: Generazione di codici di Four-Character
description: Generazione di codici di Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- I/O di file multimediali, codici di quattro caratteri
- I/O di file, codici di quattro caratteri
- input e output (I/O), codici di quattro caratteri
- I/O (input e output), codici di quattro caratteri
- codici di quattro caratteri
- mmioStringToFOURCC (funzione)
- mmioFOURCC (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725122"
---
# <a name="generating-four-character-codes"></a>Generazione di codici di Four-Character

È possibile usare la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) o la funzione [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) per generare codici di quattro caratteri. Nell'esempio seguente viene usato **mmioFOURCC** per generare un codice di quattro caratteri per "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



Nell'esempio seguente viene usato [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) per generare un codice di quattro caratteri per "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Il secondo parametro in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifica i flag per la conversione della stringa in un codice di quattro caratteri. Se si specifica il \_ flag TOUPPER MMIO, **mmioStringToFOURCC** converte tutti i caratteri alfabetici nella stringa in lettere maiuscole. Questa operazione è utile quando è necessario specificare un codice di quattro caratteri per identificare una procedura di I/O personalizzata perché i codici di quattro caratteri che identificano i nomi di estensione di file devono essere tutti in maiuscolo.

 

 