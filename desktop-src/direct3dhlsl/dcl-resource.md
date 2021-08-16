---
title: dcl_resource (sm4 - asm)
description: Risorsa dcl \_ (sm4 - asm)
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f23fac2f6671584c69ecad045d13e885e86fb260164675da3bc51f7edf847f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515636"
---
# <a name="dcl_resource-sm4---asm"></a>Risorsa dcl \_ (sm4 - asm)

Dichiara una risorsa di input shader non multicampionata.



| dcl \_ resource *tN,* *resourceType,* *returnType(s)* |
|-----------------------------------------------------|



 

Dichiara una risorsa di input shader multicampionata.



| dcl \_ resource *tN,* *resourceType size \[ \] NN,* *returnType(s)* |
|---------------------------------------------------------------|



 



| Elemento                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[in \] Registro di trama, dove *N* è un numero intero che indica il numero di registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*Resourcetype*<br/>                                   | \[in \] Qualsiasi tipo di oggetto elencato nella pagina [texture-object.](dx-graphics-hlsl-to-type.md)<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ size \] NN*<br/> | \[in \] un tipo di oggetto Texture2D o Texture2DArray (vedere la pagina [texture-object);](dx-graphics-hlsl-to-type.md) *size* è un numero intero facoltativo che indica il numero di elementi nella matrice. *NN* è un numero intero che indica il numero di multicampionamenti.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*<br/>                               | \[in tipo restituito per componente che è uno \] dei seguenti: UNORM, SNORM, SINT, UINT o FLOAT. Il numero di tipi restituiti può essere minimo 1 (se tutti i componenti sono dello stesso tipo), ma può essere fino a quattro.<br/>                                          |



 

È possibile accedere a una risorsa in HLSL usando [load.](dx-graphics-hlsl-to-load.md) È anche possibile accedere a una trama non multicampionata usando uno dei metodi di esempio dell'oggetto [trama](dx-graphics-hlsl-to-type.md) HLSL.

Se una risorsa è associata a una fase dello shader, il formato della risorsa verrà convalidato rispetto al tipo restituito.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





