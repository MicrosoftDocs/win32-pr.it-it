---
title: Funzione ByteAddressBuffer::Load2(uint)
description: Ottiene due valori. | Funzione ByteAddressBuffer::Load2(uint)
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- HLSL della funzione Load2
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fac3b1cd0fffca1a68089c3c21bfd5d6aea5f270493319b044a0bbe290d88a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845731"
---
# <a name="byteaddressbufferload2uint-function"></a>Funzione ByteAddressBuffer::Load2(uint)

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
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




