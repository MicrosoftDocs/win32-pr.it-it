---
title: Funzione ByteAddressBuffer::Load3(uint)
description: Ottiene tre valori. | Funzione ByteAddressBuffer::Load3(uint)
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- HLSL della funzione Load3
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510011"
---
# <a name="byteaddressbufferload3uint-function"></a>Funzione ByteAddressBuffer::Load3(uint)

Ottiene tre valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*address* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint3**

Tre valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




