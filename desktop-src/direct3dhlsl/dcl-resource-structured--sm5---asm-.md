---
title: dcl_resource strutturato (sm5 - asm)
description: Dichiarare un input della risorsa shader e assegnarlo a t\ - un registro segnaposto per la risorsa. | dcl_resource strutturato (sm5 - asm)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec0bc0b818b345c62bb48ae6f5db68671127110ed06a85c988f8a0449fd490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285894"
---
# <a name="dcl_resource-structured-sm5---asm"></a>Strutturata risorsa dcl \_ (sm5 - asm)

Dichiarare un input della risorsa shader e assegnarlo a un registro segnaposto per \# la risorsa.



| dcl \_ resource \_ structured dstSRV, structByteStride |
|----------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[in Un registro t dichiarato come riferimento a shaderResourceView di un buffer strutturato con lo stride specificato che deve essere associato \] \# allo slot SRV \# nell'API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] uint che specifica le dimensioni della struttura in byte nel buffer dichiarato. Il valore deve essere maggiore di zero.<br/>                                   |



 

## <a name="remarks"></a>Commenti

Il contenuto della struttura non ha alcun tipo. Le operazioni eseguite sulla memoria possono interpretare implicitamente i dati come con un tipo .

Le istruzioni che fanno riferimento a un oggetto strutturato t accettano un indirizzo 2D, in cui il primo componente seleziona lo struct e il secondo componente seleziona l'offset all'interno dello struct, multiplo di \# \[ \] \[ 32 \] bit.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





