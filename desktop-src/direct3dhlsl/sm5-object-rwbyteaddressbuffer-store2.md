---
title: Funzione RWByteAddressBuffer::Store2
description: Imposta due valori.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- HLSL della funzione Store2
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 723c2f895790618a14d6603acacb7e106a936ad5262696ef553dafa72c1332c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853311"
---
# <a name="store2-function"></a>Funzione Store2

Imposta due valori.

## <a name="syntax"></a>Sintassi

``` syntax
void Store2(
  in uint address,
  in uint2 values
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

Tipo: **uint2**

Due valori di input.

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

 

 




