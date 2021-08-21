---
title: ld_raw (sm5 - asm)
description: Lettura ad accesso casuale di componenti da 1 a 4 a 32 bit da un buffer non elaborato.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85fd8ec84b574d506a02812b20f4728e3f7a996ec76ad8569645d4c1643b0ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511091"
---
# <a name="ld_raw-sm5---asm"></a>ld \_ raw (sm5 - asm)

Lettura ad accesso casuale di componenti da 1 a 4 a 32 bit da un buffer non elaborato.



| ld \_ raw dst0 \[ \] .mask, srcByteOffset \[ .select \_ \] component, src0 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] Specifica l'offset da cui leggere.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] Componente da leggere. <br/>                     |



 

## <a name="remarks"></a>Commenti

*src0* deve essere:

-   Qualsiasi fase shader: SRV (t \# )ld st
-   Shader di calcolo o pixel shader: UAV (u \# )
-   Shader di calcolo: memoria condivisa del gruppo di thread (g \# )

*srcByteOffset* specifica il valore di base a 32 bit in memoria per una finestra di 4 valori sequenziali a 32 bit in cui è possibile leggere i dati, a seconda dello swizzle e della maschera su altri parametri.

I dati letti dal buffer non elaborato sono equivalenti allo pseudocodice seguente: dove sono disponibili l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

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

Fuori dai limiti che si indirizzano a u /t di qualsiasi componente \# \# a 32 bit specificato, restituisce 0 per tale componente.

I limiti di indirizzamento su g (i limiti di quel particolare g , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit specificato restituisce un risultato \# \# non definito.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per gli UAV per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e SRV.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





