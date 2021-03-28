---
title: texreg2ar-PS
description: Interpreta i componenti di colore alfa e rosso del registro di origine come dati degli indirizzi di trama (u, v) per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473454"
---
# <a name="texreg2ar---ps"></a>texreg2ar-PS

Interpreta i componenti di colore alfa e rosso del registro di origine come dati degli indirizzi di trama (u, v) per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2ar DST, src |
|--------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di rimapping dello spazio colore.

Ecco un esempio della sequenza seguita dall'istruzione:

<dl> Tex t (n)  
texreg2ar t (m), t (n) dove m > n  
La prima istruzione carica il colore della trama (RGBA)  
in Register TN  
Tex TN  
La seconda istruzione esegue il mapping del colore  
t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> utilizzo di t (n)<sub>AR</sub> come coordinate
</dl>

\_non è possibile usare BX2 nel registro src per le istruzioni texreg2ar o [texreg2gb-PS](texreg2gb---ps.md) .

Per questa istruzione, il registro di origine deve usare dati non firmati. L'utilizzo di dati firmati o misti nel registro di origine produrrà risultati non definiti. Per ulteriori informazioni, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 