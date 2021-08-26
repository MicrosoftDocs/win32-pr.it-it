---
title: " Direttiva pragma"
description: Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo al tempo stesso la compatibilità complessiva con i linguaggi C e C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Direttiva pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024611"
---
# <a name="pragma-directive"></a>\#Direttiva pragma

Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo al tempo stesso la compatibilità complessiva con i linguaggi C e C++.



| \#pragma *token-string* |
|-------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Serie di caratteri che fornisce istruzioni e argomenti del compilatore specifici. Questo parametro è soggetto all'espansione delle macro. <br/> |



 

## <a name="remarks"></a>Commenti

Se il compilatore trova un pragma che non riconosce, genera un avviso, ma la compilazione continua.

Il compilatore HLSL riconosce i pragma seguenti:

-   [Def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [matrice \_ di tipo pack](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





