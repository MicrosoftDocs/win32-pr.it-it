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
ms.openlocfilehash: 3c7929a7ebab01b17aca3e11cb98de8796bf568cd08a3a7b04d8f3395f531d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067911"
---
# <a name="precise"></a>Preciso

Disabilitazione per istruzione del refactoring aritmetico.



| precise (maschera componente) |
|--------------------------|



 

Questo modificatore richiede il flag di shader globale "REFACTORING \_ ALLOWED". Quando è presente REFACTORING ALLOWED, è possibile forzare i risultati dei singoli componenti delle singole istruzioni a rimanere precisi o non refactoring da parte di compilatori \_ o driver. Se i [](mad--sm4---asm-.md) componenti di un'istruzione vengono contrassegnati come **precisi,** l'hardware deve eseguire un'istruzione di tipo **"matto"** o l'equivalente esatto e non può dividerlo in una moltiplicazione seguita da un'aggiunta. Al contrario, una moltiplicazione seguita da un elemento add, in cui uno o entrambi sono contrassegnati come **precisi,** non può essere unito in un oggetto **fuso.**

Se reFACTORING \_ ALLOWED non è stato specificato, il **modificatore precise** non è consentito. Non è necessario perché tutto è preciso. Il **modificatore precise** influisce su qualsiasi operazione, non solo aritmetica.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo modificatore è supportato nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di istruzione del modello shader 5](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




