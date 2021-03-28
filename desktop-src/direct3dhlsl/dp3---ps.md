---
title: DP3-PS
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981407"
---
# <a name="dp3---ps"></a>DP3-PS

Calcola il prodotto del punto a tre componenti dei registri di origine.

## <a name="syntax"></a>Sintassi



| DP3 DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Questa istruzione viene eseguita nella pipeline vettoriale, scrivendo sempre nei canali dei colori. Per la versione 1 \_ 4, questa istruzione usa ancora la pipeline vettoriale ma può scrivere su qualsiasi canale.

Un'istruzione con una maschera di scrittura di destinazione Register. RGB (. xyz) può essere co-emessa con DP3, come illustrato di seguito.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



L'istruzione DP3 può essere modificata tramite il modificatore dell'argomento di input del [Registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) applicato ai relativi argomenti di input se non sono già stati espansi nell'intervallo dinamico con segno. Per uno shader di illuminazione, il modificatore dell'istruzione di saturazione ( \_ Sat) viene spesso usato per bloccare i valori negativi a nero, come illustrato nell'esempio seguente.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




