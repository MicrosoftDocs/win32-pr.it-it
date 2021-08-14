---
title: Funzione abort (Corecrt \_ terminate.h)
description: Invia un messaggio di errore alla coda di informazioni e termina la chiamata di disegno o invio corrente in esecuzione.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Funzione abort HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a708d2893a19369d2db42f4551e3fafa4a1ff7a4680bf8676de32f79764289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795525"
---
# <a name="abort-function"></a>abort (funzione)

Invia un messaggio di errore alla coda di informazioni e termina la chiamata di disegno o invio corrente in esecuzione.

## <a name="syntax"></a>Sintassi

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

 
</dt> <dd>

nessuno

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione non esegue alcuna operazione sui rasterizzatori che non la supportano.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o versione successiva.](dx-graphics-hlsl-sm3.md) | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ terminate.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





