---
title: 'Funzione RWStructuredBuffer:: Load (int)'
description: 'Legge i dati del buffer. | Funzione RWStructuredBuffer:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995365"
---
# <a name="rwstructuredbufferloadint-function"></a>Funzione RWStructuredBuffer:: Load (int)

Legge i dati del buffer.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **int**

Posizione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




