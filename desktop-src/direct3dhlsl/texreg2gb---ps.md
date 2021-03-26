---
title: texreg2gb-PS
description: Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976690"
---
# <a name="texreg2gb---ps"></a>texreg2gb-PS

Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2gb DST, src |
|--------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di rimapping dello spazio colore.

Di seguito è riportato un esempio della sequenza che segue l'istruzione.

<dl> Tex t (n)  
texreg2gb t (m), t (n) dove m > n  
La prima istruzione carica il colore della trama (RGBA)  
in Register TN  
Tex TN  
La seconda istruzione esegue il mapping del colore  
t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> usando t (n)<sub>GB</sub> come coordinate
</dl>

\_non è possibile usare BX2 nel registro src per le istruzioni [texreg2ar-PS](texreg2ar---ps.md) o texreg2gb.

Per questa istruzione, il registro di origine deve usare dati non firmati. L'utilizzo di dati firmati o misti nel registro di origine produrrà risultati non definiti. Per ulteriori informazioni, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 