---
title: texdp3tex-PS
description: Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992976"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Esegue un prodotto punto a tre componenti e usa il risultato per eseguire una ricerca di trama 1D.

## <a name="syntax"></a>Sintassi



| texdp3tex DST, src |
|--------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
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



Di seguito sono illustrati in modo più dettagliato il modo in cui vengono eseguiti il prodotto e la ricerca di trama.

L'istruzione texdp3tex esegue un prodotto dot a tre componenti.

u ' = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Il risultato viene usato per campionare la trama in fase di trama m eseguendo una ricerca 1D.

t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> using (u ',0, 0) As coordinates

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




