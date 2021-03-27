---
title: 'Funzione RWStructuredBuffer:: IncrementCounter (Httpserv. h)'
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
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355494"
---
# <a name="incrementcounter-function"></a>IncrementCounter (funzione)

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

Per il corretto funzionamento di questo metodo, è necessario che nella visualizzazione di accesso non ordinato associato sia impostato il [**\_ \_ \_ \_ contatore dei flag UAV del buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante la creazione.

Una risorsa strutturata può essere ulteriormente indicizzata in base ai nomi dei componenti delle strutture.

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

 

