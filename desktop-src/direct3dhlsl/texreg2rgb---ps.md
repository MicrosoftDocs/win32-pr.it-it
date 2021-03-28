---
title: texreg2rgb-PS
description: Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati degli indirizzi di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516495"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-PS

Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati degli indirizzi di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2rgb DST, src |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di rimapping dello spazio colore. Supporta le coordinate bidimensionali (2D) e tridimensionali (3D). Può essere usato come [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md) per modificare il mapping dei dati 2D. Tuttavia, questa istruzione supporta anche i dati 3D, in modo che possano essere utilizzati con le mappe del cubo e le trame del volume 3D.

Di seguito è riportato un esempio della sequenza che segue l'istruzione.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Di seguito sono riportati altri dettagli sul modo in cui viene eseguito il mapping.

<dl> La prima istruzione carica il colore della trama (RGBA) nel registro TN  
Tex TN  
La seconda istruzione esegue il mapping del colore  
t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> utilizzo di t (n)<sub>RGB</sub> come coordinate
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




