---
title: Funzione ByteAddressBuffer::Load4(uint)
description: Ottiene quattro valori. | Funzione ByteAddressBuffer::Load4(uint)
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
keywords:
- Funzione Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623c62ce9038d4e06cfbb952808aeb0530cb2e937c83578d9ef0e71c9b0a038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510001"
---
# <a name="byteaddressbufferload4uint-function"></a>Funzione ByteAddressBuffer::Load4(uint)

Ottiene quattro valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint4 Load4(
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

Tipo: **uint4**

Quattro valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load4](byteaddressbuffer-load4.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




