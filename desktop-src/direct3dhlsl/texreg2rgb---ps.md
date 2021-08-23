---
title: texreg2rgb - ps
description: Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati dell'indirizzo della trama per campionare la trama nella fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c32ee8e6b1560bfcebf6a914a45be2c74b19e94568c9d4e9b24084bf56c3f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043049"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb - ps

Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati dell'indirizzo della trama per campionare la trama nella fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2rgb dst, src |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di mapping dello spazio colore. Supporta coordinate bidimensionali (2D) e tridimensionali (3D). Può essere usato esattamente come [texreg2ar - ps](texreg2ar---ps.md) o [texreg2gb - ps per](texreg2gb---ps.md) modificare il mapping dei dati 2D. Tuttavia, questa istruzione supporta anche i dati 3D in modo che possano essere usati con mappe di cubi e trame di volume 3D.

Di seguito è riportato un esempio della sequenza che segue l'istruzione .


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Di seguito sono fornite informazioni più dettagliate su come viene eseguita la ridefinitura del mapping.

<dl> La prima istruzione carica il colore della trama (RGBA) nel registro tn  
tex tn  
La seconda istruzione modifica il mapping del colore  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>RGB</sub> come coordinate
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




