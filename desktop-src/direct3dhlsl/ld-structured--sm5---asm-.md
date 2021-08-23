---
title: ld_structured (sm5 - asm)
description: Lettura ad accesso casuale di componenti da 1 a 4 a 32 bit da un buffer strutturato.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562311"
---
# <a name="ld_structured-sm5---asm"></a>ld \_ strutturato (sm5 - asm)

Lettura ad accesso casuale di componenti da 1 a 4 a 32 bit da un buffer strutturato.



| : ld \_ structured dst0 \[ \] .mask, srcAddress \[ .select \_ \] component, srcByteOffset \[ .select \_ \] component, src0 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Indirizzo dei risultati dell'operazione.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[in \] Specifica l'indice della struttura da leggere.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] Specifica l'offset di byte nella struttura da cui iniziare la lettura. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Buffer da cui leggere. Questo parametro deve essere SRV (t \# ), UAV (u \# ). Nello shader di calcolo può anche essere memoria condivisa del gruppo di thread (g \# ). <br/> |



 

## <a name="remarks"></a>Commenti

I dati letti dalla struttura sono equivalenti allo pseudocodice seguente: dove sono disponibili l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Questo pseudocodice mostra il funzionamento dell'operazione, ma i dati effettivi non devono essere archiviati in modo lineare. Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.

Fuori dai limiti che si indirizzano a u /t di qualsiasi componente a 32 bit specificato restituisce 0 per tale componente, ad eccezione del fatto che se \# \# *srcByteOffset*, più swizzle è ciò che causa l'accesso all'utente /t fuori dai limiti, il valore restituito per tutti i componenti \# \# non è definito.

I limiti di indirizzamento su g (i limiti di quel particolare g , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit specificato restituisce un risultato \# \# non definito.

*srcByteOffset è* un argomento separato da *srcAddress* perché è in genere un valore letterale. Questa separazione dei parametri non è stata eseguita per gli atomici nella memoria strutturata.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

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



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





