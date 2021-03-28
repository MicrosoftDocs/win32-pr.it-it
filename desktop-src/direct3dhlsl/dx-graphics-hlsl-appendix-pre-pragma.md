---
title: " pragma (direttiva)"
description: Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo la compatibilità complessiva con i linguaggi C e C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma directive HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045738"
---
# <a name="pragma-directive"></a>\#pragma (direttiva)

Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo la compatibilità complessiva con i linguaggi C e C++.



| \#pragma *-stringa di token* |
|-------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*<br/> | Serie di caratteri che fornisce un'istruzione e argomenti specifici del compilatore. Questo parametro è soggetto all'espansione della macro. <br/> |



 

## <a name="remarks"></a>Commenti

Se il compilatore trova un pragma che non riconosce, genera un avviso, ma la compilazione continua.

Il compilatore HLSL riconosce i seguenti pragma:

-   [def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [matrice di pacchetti \_](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





