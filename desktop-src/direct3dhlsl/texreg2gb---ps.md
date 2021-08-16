---
title: texreg2gb - ps
description: Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama nella fase corrispondente al numero del registro di destinazione.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505749"
---
# <a name="texreg2gb---ps"></a>texreg2gb - ps

Interpreta i componenti di colore verde e blu del registro di origine come dati dell'indirizzo di trama per campionare la trama nella fase corrispondente al numero del registro di destinazione.

## <a name="syntax"></a>Sintassi



| texreg2gb dst, src |
|--------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Questa istruzione è utile per le operazioni di ridefinizione dello spazio dei colori.

Di seguito è riportato un esempio della sequenza che segue l'istruzione .

<dl> tex t(n)  
texreg2gb t(m), t(n) dove m > n  
La prima istruzione carica il colore della trama (RGBA)  
into register tn  
tex tn  
La seconda istruzione modifica il mapping del colore  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando t(n)<sub>GB</sub> come coordinate
</dl>

\_bx2 non può essere usato nel registro src per le istruzioni [texreg2ar - ps](texreg2ar---ps.md) o texreg2gb.

Per questa istruzione, il registro di origine deve usare dati non firmati. L'uso di dati firmati o misti nel registro di origine produrrà risultati non definiti. Per altre informazioni, vedere [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 