---
title: dcl_resource (SM4-ASM)
description: '\_risorsa DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719471"
---
# <a name="dcl_resource-sm4---asm"></a>\_risorsa DCL (SM4-ASM)

Dichiara una risorsa di input shader non multicampionata.



| \_risorsa DCL *TN*, *ResourceType*, *ReturnType (s)* |
|-----------------------------------------------------|



 

Dichiara una risorsa di input shader multicampionata.



| \_risorsa DCL *TN*, *\[ dimensioni ResourceType \] nn*, *returnType* |
|---------------------------------------------------------------|



 



| Elemento                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[nel \] Registro di trama, dove *N* è un numero intero che indica il numero di registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[in \] qualsiasi tipo di oggetto elencato nella pagina [texture-Object](dx-graphics-hlsl-to-type.md) .<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*dimensioni del resourceType \[ \] nn*<br/> | \[in \] un tipo di oggetto Texture2D o Texture2DArray (vedere la pagina [texture-Object](dx-graphics-hlsl-to-type.md) ); *size* è un numero intero facoltativo che indica il numero di elementi nella matrice. *Nn* è un numero intero che indica il numero di campionamenti.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*<br/>                               | \[nel \] tipo restituito per componente che è uno dei seguenti: UNORM, russar, Sint, uint o float. Il numero di tipi restituiti può essere pari a 1 (se tutti i componenti sono dello stesso tipo), ma può essere costituito da un massimo di quattro.<br/>                                          |



 

È possibile accedere a una risorsa in HLSL usando [Load](dx-graphics-hlsl-to-load.md); è possibile accedere a una trama non multicampionato anche usando uno dei metodi di esempio dell' [oggetto HLSL texture](dx-graphics-hlsl-to-type.md) .

Se una risorsa è associata a una fase shader, il formato della risorsa verrà convalidato in base al tipo restituito.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





