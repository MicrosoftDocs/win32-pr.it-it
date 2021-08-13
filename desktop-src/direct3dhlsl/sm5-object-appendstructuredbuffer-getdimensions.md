---
title: Funzione AppendStructuredBuffer::GetDimensions
description: Ottiene le dimensioni della risorsa. | Funzione AppendStructuredBuffer::GetDimensions
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Funzione GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790652"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>Funzione AppendStructuredBuffer::GetDimensions

Ottiene le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*NumStructs* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Numero di strutture.

</dd> <dt>

*stride* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Numero di byte in ogni elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




