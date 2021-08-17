---
title: Funzione RWByteAddressBuffer::GetDimensions
description: Ottiene la lunghezza del buffer. | Funzione RWByteAddressBuffer::GetDimensions
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 2271f563251cfdb9c6f2a2174c91dc8c271c7354a2b10b9b2e7e55cb4af09d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725146"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>Funzione RWByteAddressBuffer::GetDimensions

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

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




