---
title: Funzione RWByteAddressBuffer::Load2(uint)
description: Ottiene due valori. | Funzione RWByteAddressBuffer::Load2(uint)
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Funzione Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f71fd2d0585803fb10de3fddfa29c10838d73e32ba7d63b5619be91b042cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725058"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>Funzione RWByteAddressBuffer::Load2(uint)

Ottiene due valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint2 Load2(
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

Tipo: **uint2**

Due valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load2](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




