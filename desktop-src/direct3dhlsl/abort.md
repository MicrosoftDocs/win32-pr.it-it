---
title: funzione Abort (Corecrt \_ Terminate. h)
description: Invia un messaggio di errore alla coda di informazioni e termina la chiamata di progetto o di invio corrente eseguita.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- funzione Abort HLSL
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
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982635"
---
# <a name="abort-function"></a>abort (funzione)

Invia un messaggio di errore alla coda di informazioni e termina la chiamata di progetto o di invio corrente eseguita.

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

Questa operazione non esegue alcuna operazione nei rasterizzatori che non lo supportano.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o versione successiva.](dx-graphics-hlsl-sm3.md) | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ termina. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





