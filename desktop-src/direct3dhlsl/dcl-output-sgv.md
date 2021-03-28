---
title: dcl_output_sgv (SM4-ASM)
description: '\_ \_ SGV di output di DCL (SM4-ASM)'
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398300"
---
# <a name="dcl_output_sgv-sm4---asm"></a>\_ \_ SGV di output di DCL (SM4-ASM)

Dichiara un registro di output che contiene un parametro del [valore di sistema](dx-graphics-hlsl-semantics.md) .



| \_ \_ SGV di output di DCL su *\[ \] . mask*, *systemValue* |
|-----------------------------------------------|



 



| Elemento                                                                                                                               | Descrizione                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[in \] un registro dei dati di output; *N* è un numero intero che indica il numero di registro.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. mask\]*<br/>                                                         | \[in \] facoltativo. Maschera di componenti (con estensione xyzw) che specifica quale dei componenti del registro utilizzare.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[nel \] nome del valore di sistema che è una stringa (vedere [semantica del valore di sistema](dx-graphics-hlsl-semantics.md)) senza il prefisso "SV \_ ".<br/> |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader in linguaggio assembly usando il modello di Shader 4.

## <a name="example"></a>Esempio

Ecco un esempio.


```
dcl_output_sgv o4.x, primitiveID
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

 

 





