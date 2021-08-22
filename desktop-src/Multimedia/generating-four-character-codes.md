---
title: Generazione di Four-Character personalizzati
description: Generazione di Four-Character personalizzati
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- I/O di file multimediali, codici a quattro caratteri
- I/O file, codici a quattro caratteri
- input e output (I/O),codici a quattro caratteri
- I/O (input e output),codici a quattro caratteri
- codici di quattro caratteri
- Funzione mmioStringToFOURCC
- Macro mmioFOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96dd724876a3c4b6ac37424b49411edac5929c61d1fcf6c8c18275b1d6ae9dd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785311"
---
# <a name="generating-four-character-codes"></a>Generazione di Four-Character personalizzati

È possibile usare la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) o la funzione [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) per generare codici di quattro caratteri. L'esempio seguente **usa mmioFOURCC per** generare un codice di quattro caratteri per "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



L'esempio seguente [**usa mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) per generare un codice di quattro caratteri per "WAVE".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Il secondo parametro in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifica i flag per la conversione della stringa in un codice di quattro caratteri. Se si specifica il flag MMIO \_ TOUPPER, **mmioStringToFOURCC** converte tutti i caratteri alfabetici nella stringa in lettere maiuscole. Ciò è utile quando è necessario specificare un codice di quattro caratteri per identificare una procedura di I/O personalizzata perché i codici a quattro caratteri che identificano i nomi delle estensioni di file devono essere tutti in maiuscolo.

 

 