---
title: Funzione RWStructuredBuffer::IncrementCounter (Httpserv.h)
description: Incrementa il contatore nascosto dell'oggetto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Funzione IncrementCounter HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095171"
---
# <a name="incrementcounter-function"></a>Funzione IncrementCounter

Incrementa il contatore nascosto dell'oggetto.

## <a name="syntax"></a>Sintassi

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Valore del contatore pre-incrementato.

## <a name="remarks"></a>Commenti

Per il funzionamento di questo metodo, la vista di accesso non ordinata associata deve avere [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) impostato durante la creazione.

Una risorsa strutturata può essere ulteriormente indicizzata in base ai nomi dei componenti delle strutture.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

