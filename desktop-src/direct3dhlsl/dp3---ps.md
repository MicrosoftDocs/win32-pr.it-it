---
title: dp3 - ps
description: Calcola il prodotto del punto a tre componenti dei registri di origine. | dp3 - ps
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49e957078832f11885ea82baf8438d712394133eb77ad8eeaba705ff0d32a9d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024631"
---
# <a name="dp3---ps"></a>dp3 - ps

Calcola il prodotto del punto a tre componenti dei registri di origine.

## <a name="syntax"></a>Sintassi



| dp3 dst, src0, src1 |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente illustra le operazioni eseguite:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Questa istruzione viene eseguita nella pipeline vettoriale, scrivendo sempre nei canali di colore. Per la versione \_ 1 4, questa istruzione usa ancora la pipeline vettoriale, ma può scrivere in qualsiasi canale.

Un'istruzione con una maschera di scrittura con estensione rgb (.xyz) del registro di destinazione può essere rilasciata con dp3 come illustrato di seguito.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



L'istruzione dp3 può essere modificata usando il modificatore dell'argomento di input [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( bx2) applicato ai relativi argomenti di input se non sono già espansi nell'intervallo dinamico \_ con segno. Per uno shader di illuminazione, il modificatore di istruzione saturate (sat) viene spesso usato per impostare i valori negativi sul nero, come illustrato \_ nell'esempio seguente.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




