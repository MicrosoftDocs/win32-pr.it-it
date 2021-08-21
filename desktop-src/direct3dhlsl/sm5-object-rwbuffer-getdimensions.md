---
title: Funzione RWBuffer::GetDimensions
description: Ottiene la lunghezza del buffer. | Funzione RWBuffer::GetDimensions
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 586f266fea0dbc035e8ff3a61e39cb18a7102d792ee05c44345a1b702cc1b574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118241"
---
# <a name="rwbuffergetdimensions-function"></a>Funzione RWBuffer::GetDimensions

Ottiene la lunghezza del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

Tipo: **uint**

Lunghezza, in byte, del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




