---
title: def (direttiva pragma)
description: Direttiva pragma che alloca manualmente un registro shader a virgola mobile.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Direttiva pragma def HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992912"
---
# <a name="def-pragma-directive"></a>def (direttiva pragma)

Direttiva pragma che alloca manualmente un registro shader a virgola mobile.



| \#pragma def ( *target*, *Register*, *val1*, *val2*,*Val3*, *Val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                        | Descrizione                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*destinazione*<br/>       | Destinazione contenente il registro da allocare. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*Registro*<br/> | Registro shader a virgola mobile da allocare. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Primo byte del valore da allocare al registro specificato. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Secondo byte del valore da allocare al registro specificato. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Terzo byte del valore da allocare al registro specificato. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Quarto byte del valore da allocare al registro specificato. <br/> |



 

## <a name="remarks"></a>Commenti

Il pragma def consente a uno sviluppatore di precompilare un registro shader a virgola mobile con il valore specificato. Questo pragma viene usato raramente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (direttiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





