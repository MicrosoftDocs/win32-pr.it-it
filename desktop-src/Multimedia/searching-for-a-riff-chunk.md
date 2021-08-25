---
title: Ricerca di un blocco RIFF
description: Ricerca di un blocco RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- I/O di file multimediali, ricerca di blocchi RIFF
- I/O di file, ricerca di blocchi RIFF
- input e output (I/O), ricerca di blocchi RIFF
- I/O (input e output), ricerca di blocchi RIFF
- ricerca di un blocco RIFF
- resource interchange file format (RIFF)
- RIFF (formato di file di interscambio di risorse)
- RIFF I/O
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbb09c7777cf675ceb0f11ae84fb50a3b9deaa73910ca9e15280c3fb88c42cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782091"
---
# <a name="searching-for-a-riff-chunk"></a>Ricerca di un blocco RIFF

Nell'esempio seguente viene utilizzata la funzione [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) per cercare un blocco "RIFF" con un tipo di formato "WAVE" per verificare che il file appena aperto sia un file waveform-audio.


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 