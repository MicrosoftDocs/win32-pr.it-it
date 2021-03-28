---
title: Preciso
description: Disabilitazione per istruzione del refactoring aritmetico.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516477"
---
# <a name="precise"></a>Preciso

Disabilitazione per istruzione del refactoring aritmetico.



| preciso (maschera componenti) |
|--------------------------|



 

Questo modificatore richiede il flag di shader globale "refactoring \_ allowed". Quando è presente il refactoring \_ consentito, i risultati dei singoli componenti delle singole istruzioni possono essere costretti a rimanere precisi o non sottoposti a refactoring dai compilatori o dai driver. Se i componenti di un'istruzione [**MAD**](mad--sm4---asm-.md) sono contrassegnati come **precisi**, l'hardware deve eseguire un'istruzione **MAD** o l'equivalente esatto e non può suddividerlo in una moltiplicazione seguita da un Add. Viceversa, un valore Multiply seguito da un oggetto Add, in cui uno o entrambi i flag sono contrassegnati come **precisi**, non possono essere Uniti in un oggetto **MAD** con fusibile.

Se il refactoring \_ consentito non è stato specificato, il modificatore **preciso** non è consentito. Non è necessario perché tutto è preciso. Il modificatore **preciso** influiscono su qualsiasi operazione, non solo aritmetica.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo modificatore è supportato nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di istruzioni Model 5 shader](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




