---
title: ld_raw (SM5-ASM)
description: Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer non elaborato.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976399"
---
# <a name="ld_raw-sm5---asm"></a>LD \_ RAW (SM5-ASM)

Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer non elaborato.



| LD \_ RAW dst0 \[ . mask \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] specifica l'offset da cui leggere.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[nel \] componente da leggere. <br/>                     |



 

## <a name="remarks"></a>Commenti

*src0* deve essere:

-   Qualsiasi fase dello shader: SRV (t \# ) LD St
-   Compute shader o pixel shader: UAV (u \# )
-   Compute Shader: memoria condivisa del gruppo di thread (g \# )

*srcByteOffset* specifica il valore di base a 32 bit in memoria per una finestra di 4 valori sequenziali a 32 bit in cui è possibile leggere i dati, a seconda di swizzle e maschera su altri parametri.

I dati letti dal buffer non elaborato sono equivalenti al seguente pseudocodice: dove abbiamo l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Il superamento dei limiti per u \# /t \# di un determinato componente a 32 bit restituisce 0 per quel componente.

All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, restituiscono un risultato non definito.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per UAV per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





