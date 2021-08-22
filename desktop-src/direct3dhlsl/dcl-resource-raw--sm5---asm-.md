---
title: dcl_resource non elaborato (sm5 - asm)
description: Dichiarare un input della risorsa shader e assegnarlo a t\ - un registro segnaposto per la risorsa. | dcl_resource non elaborato (sm5 - asm)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b228ccc8bba795e700135bfe9ba54ea311536745b7e12eea03a8963d16e73285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793086"
---
# <a name="dcl_resource-raw-sm5---asm"></a>dcl \_ resource raw (sm5 - asm)

Dichiarare un input della risorsa shader e assegnarlo a un registro segnaposto per \# la risorsa.



| dcl \_ resource \_ raw dstSRV |
|---------------------------|



 



| Elemento                                                                                           | Descrizione                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[in \] Un registro t dichiarato come riferimento a \# shaderResourceView di un buffer non elaborato.<br/> |



 

## <a name="remarks"></a>Commenti

Il contenuto della struttura non ha alcun tipo. Le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come con un tipo.

Le istruzioni che fanno riferimento a un t non elaborato accettano un indirizzo 1D, un valore senza segno a 32 bit che specifica l'offset dei byte in una posizione \# allineata a 32 bit nel buffer. L'indirizzo deve essere un multiplo di 4 (byte).

Le viste associate a t dichiarate come non elaborate devono avere raw specificate durante la creazione. In caso contrario, il comportamento quando si accede \# da uno shader non è definito.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.

Questa istruzione si applica alle fasi dello shader seguenti:



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

 

 





