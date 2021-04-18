---
title: Ricerca di un blocco RIFF
description: Ricerca di un blocco RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- I/O file multimediale, ricerca di blocchi di RIFF
- I/O di file, ricerca di un blocco di RIFF
- input e output (I/O), ricerca di blocchi di RIFF
- I/O (input e output), ricerca di blocchi RIFF
- ricerca del blocco RIFF
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399029"
---
# <a name="searching-for-a-riff-chunk"></a>Ricerca di un blocco RIFF

Nell'esempio seguente viene usata la funzione [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) per cercare un blocco "riff" con un tipo di modulo "Wave" per verificare che il file che è stato appena aperto sia un file dell'audio della forma d'onda.


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



 

 