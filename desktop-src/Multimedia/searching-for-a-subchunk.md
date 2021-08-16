---
title: Ricerca di un oggetto Subchunk
description: Ricerca di un oggetto Subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- I/O di file multimediali, ricerca del blocco RIFF
- I/O di file, ricerca del blocco RIFF
- input e output (I/O), ricerca di blocchi RIFF
- I/O (input e output),ricerca del blocco RIFF
- ricerca di blocchi RIFF
- resource interchange file format (RIFF)
- RIFF (formato di file di interscambio di risorse)
- RIFF I/O
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f77cc4d3b9640e0d262a113d3c8f352bb30fce625737b1bf13dde24adbe578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371139"
---
# <a name="searching-for-a-subchunk"></a>Ricerca di un oggetto Subchunk

Nell'esempio seguente viene utilizzata la funzione [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) per cercare il blocco "FMT" nel blocco "RIFF" dell'esempio precedente.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Per cercare un blocco subchunk, ovvero qualsiasi blocco diverso da un blocco "RIFF" o "LIST", identificare il blocco padre nel parametro *lpckParent* della funzione [**mmioDescend.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)

Se non si specifica un blocco padre, la posizione del file corrente deve essere all'inizio di un blocco prima di chiamare la funzione **mmioDescend.** Se si specifica un blocco padre, la posizione del file corrente può essere in qualsiasi punto del blocco.

Se la ricerca di una subchunk ha esito negativo, la posizione del file corrente non è definita. È possibile usare la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) e il membro **dwDataOffset** della struttura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) che descrive il blocco padre per tornare all'inizio del blocco padre, come nell'esempio seguente:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Poiché **dwDataOffset** specifica l'offset all'inizio della parte di dati del blocco, è necessario cercare 4 byte dopo **dwDataOffset** per impostare la posizione del file dopo il tipo di modulo.

 

 