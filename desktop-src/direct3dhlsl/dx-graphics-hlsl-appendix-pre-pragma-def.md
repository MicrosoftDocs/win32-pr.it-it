---
title: Direttiva pragma def
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
ms.openlocfilehash: fe6961f5fd8c05f291af3634c07de6befada0efa54586796ca881bffe893bf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726441"
---
# <a name="def-pragma-directive"></a>Direttiva pragma def

Direttiva pragma che alloca manualmente un registro shader a virgola mobile.



| \#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                        | Descrizione                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*bersaglio*<br/>       | Destinazione che contiene il registro da allocare. <br/>                  |
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

[\#Direttiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





