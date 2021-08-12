---
title: store_structured (sm5 - asm)
description: Scrittura ad accesso casuale di componenti a 1-4 a 32 bit in una visualizzazione di accesso non ordinato del buffer strutturato.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a220fca330ba4198669245f0336b363c448067613e3f21fce44c9af9325bd9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285756"
---
# <a name="store_structured-sm5---asm"></a>store \_ structured (sm5 - asm)

Scrittura ad accesso casuale di componenti a 1-4 a 32 bit in una visualizzazione di accesso non ordinato del buffer strutturato.



| store \_ structured dst0 \[ .write mask , \_ \] dstAddress \[ .select component , \_ \] dstByteOffset \[ .select component , \_ \] src0 \[ .swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[in \] Indirizzo in cui scrivere.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[in \] Indice della struttura da scrivere.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] Componenti da scrivere.<br/>                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue componenti a 32 bit a 1-4 componenti scritti da \* *src0* *a dst0* in corrispondenza dell'indirizzo in *dstAddress* e *dstByteOffset*. Nessuna conversione del formato.

*dst0* deve essere un UAV (u \# ). Nello shader di calcolo può anche essere memoria condivisa del gruppo di thread (g \# ).

*dstAddress* specifica l'indice della struttura da scrivere.

La posizione dei dati scritti equivale allo pseudocodice seguente che mostra l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

Questo pseudocodice mostra il funzionamento dell'operazione, ma i dati effettivi non devono essere archiviati in modo lineare. Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.

*dst0* può avere solo una maschera di scrittura che è una delle seguenti: .x, .xy, .xyz, .xyzw. La maschera di scrittura determina il numero di componenti a 32 bit da scrivere senza lacune.

Fuori dai limiti che si indirizzano a u \# casued da *dstAddress* significa che non viene scritto nulla nella memoria fuori dai limiti.

Se *dstByteOffset*, incluso *dstWriteMask*, è ciò che causa l'accesso all'utente fuori dai limiti, l'intero contenuto \# dell'UAV diventa indefinito.

I limiti che si indirizzano a g (i limiti di quel particolare g , anziché tutta la memoria condivisa) per qualsiasi componente a 32 bit specificato causano l'indefinizione dell'intero contenuto di tutta la memoria \# \# condivisa.

*dstByteOffset è* un argomento separato da *dstAddress* perché è in genere un valore letterale. Questa separazione dei parametri non è stata eseguita per gli atomici nella memoria strutturata.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e TGSM.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





