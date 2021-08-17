---
title: dcl_output_siv (sm4 - asm)
description: dcl \_ output \_ siv (sm4 - asm)
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3035724a76aff71c2ba2b7500874365ea284f55b0bf16389b3d83c99205e606b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515679"
---
# <a name="dcl_output_siv-sm4---asm"></a>dcl \_ output \_ siv (sm4 - asm)

Dichiara un registro di output che contiene un [parametro di valore di](dx-graphics-hlsl-semantics.md) sistema.



| dcl \_ output \_ siv oN \[ *.masks* \] , *systemValue* |
|------------------------------------------------|



 



| Elemento                                                                                                                               | Descrizione                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[in \] Un registro dei dati di output; *N* è un numero intero che indica il numero di registro.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*<br/>                                                         | \[in \] Facoltativo. Maschera del componente (.xyzw) che specifica quali componenti del registro usare.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[in \] Nome del valore di sistema che è una stringa (vedere la [semantica dei valori](dx-graphics-hlsl-semantics.md)di sistema ) senza il prefisso \_ "SV".<br/> |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

## <a name="example"></a>Esempio

Di seguito sono riportati alcuni esempi.


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
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

 

 





