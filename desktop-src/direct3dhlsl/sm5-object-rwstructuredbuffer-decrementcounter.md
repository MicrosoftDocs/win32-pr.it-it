---
title: RWStructuredBuffer::D funzione ecrementCounter (Httpserv. h)
description: Decrementa il contatore nascosto dell'oggetto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Funzione DecrementCounter HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982388"
---
# <a name="decrementcounter-function"></a>DecrementCounter (funzione)

Decrementa il contatore nascosto dell'oggetto.

## <a name="syntax"></a>Sintassi

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Valore del contatore dopo il decremento.

## <a name="remarks"></a>Commenti

Per il funzionamento della visualizzazione di accesso non ordinato associato è necessario impostare il [**\_ \_ \_ \_ contatore del flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante creationfor.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Httpserv. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

