---
title: texreg2ar - ps
description: Interpreta i componenti dei colori alfa e rosso del registro di origine come dati dell'indirizzo della trama (u,v) per campionare la trama nella fase corrispondente al numero del registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee9516c43f5e8d774ef496a0e66ae1a8ee839ff3df6f2f5436caaf887f95da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284002"
---
# <a name="texreg2ar---ps"></a>texreg2ar - ps

Interpreta i componenti dei colori alfa e rosso del registro di origine come dati dell'indirizzo della trama (u,v) per campionare la trama nella fase corrispondente al numero del registro di destinazione. Il risultato viene archiviato nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2ar dst, src |
|--------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di mapping dello spazio colore.

Di seguito è riportato un esempio della sequenza che l'istruzione segue:

<dl> tex t(n)  
texreg2ar t(m), t(n) where m > n  
La prima istruzione carica il colore della trama (RGBA)  
into register tn  
tex tn  
La seconda istruzione modifica il mapping del colore  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>AR</sub> come coordinate
</dl>

\_bx2 non può essere usato nel registro src per le istruzioni texreg2ar o [texreg2gb - ps.](texreg2gb---ps.md)

Per questa istruzione, il registro di origine deve usare dati non firmati. L'uso di dati firmati o misti nel registro di origine produrrà risultati non definiti. Per altre informazioni, vedere [D3DFORMAT.](/windows/desktop/direct3d9/d3dformat)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 