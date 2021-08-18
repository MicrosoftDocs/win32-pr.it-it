---
title: texdp3tex - ps
description: Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788037"
---
# <a name="texdp3tex---ps"></a>texdp3tex - ps

Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.

## <a name="syntax"></a>Sintassi



| texdp3tex dst, src |
|--------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

I registri di trama devono usare la sequenza seguente.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Ecco altri dettagli su come viene eseguita la ricerca del prodotto punto e della trama.

L'istruzione texdp3tex esegue un prodotto punto a tre componenti.

u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Il risultato viene usato per campionare la trama nella fase della trama m eseguendo una ricerca 1D.

t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> usando (u',0,0) come coordinate

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




