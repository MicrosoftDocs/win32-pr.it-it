---
title: dcl_input vPrim (sm4 - asm)
description: dcl \_ input vPrim (sm4 - asm)
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 166111e8a4c0504589fe45727d7fc00cc4e1a90cf0e7848f09587f525294b7c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024741"
---
# <a name="dcl_input-vprim-sm4---asm"></a>dcl \_ input vPrim (sm4 - asm)

Dichiara che uno shader geometry usa il relativo registro di input scalare vPrim.



| dcl \_ input *vPrim* |
|--------------------|



 



| Elemento                                                                                       | Descrizione                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*<br/> | \[in un scalare a \] 32 bit, che può essere applicato a ogni primitiva interna in un geometry shader.<br/> |



 

Lo scalare non può essere applicato ad alcuna primitiva adiacente.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. Non è possibile creare uno shader in linguaggio assembly usando il modello shader 4.

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

 

 





