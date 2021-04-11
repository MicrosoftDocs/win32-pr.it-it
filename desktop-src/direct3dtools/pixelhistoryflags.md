---
description: Enumerazione contenente i flag utilizzati per descrivere il risultato di una cronologia pixel. Vedere PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124158"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Enumerazione PIXELHISTORYFLAGS

Enumerazione contenente i flag utilizzati per descrivere il risultato di una cronologia pixel. Vedere PixelHistoryOperation.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**\_InitialValue PHF**  
Flag che corrisponde al valore di colore iniziale (prima del frame).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Clear**  
Flag che corrisponde al risultato del colore non crittografato.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF- \_ disegni**  
Flag che corrisponde al risultato del colore di traccia.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**\_FINALVALUE PHF**  
Flag che corrisponde al risultato del colore finale.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**\_HASCOLOR PHF**  
Flag che corrisponde a se il risultato del colore è presente nello struct PixelHistoryOperation.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**\_HASFBCOLOR PHF**  
Flag che corrisponde a se il risultato del colore del buffer finale è presente nello struct PixelHistoryOperation.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**\_errore PHF**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**\_VERTEXPROCESSINGSKIPPED PHF**  
Non usato.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**\_MODIFYRESOURCE PHF**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**\_CANNOTRUNFULLDEPTHSTENCILTEST PHF**  
Flag che corrisponde a non essere in grado di eseguire il test di profondità o stencil.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



