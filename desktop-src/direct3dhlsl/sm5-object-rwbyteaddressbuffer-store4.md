---
title: Funzione RWByteAddressBuffer::Store4
description: Imposta quattro valori.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Funzione Store4 HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc644647616f6c6654023be23aaa8e420dbb85ad439547d1befd44c0ea7b210c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789972"
---
# <a name="store4-function"></a>Funzione Store4

Imposta quattro valori.

## <a name="syntax"></a>Sintassi

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*address* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> <dt>

*valori* \[ Pollici\]
</dt> <dd>

Tipo: **uint4**

Quattro valori di input.

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

 

 




