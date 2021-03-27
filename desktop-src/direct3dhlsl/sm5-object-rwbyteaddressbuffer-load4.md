---
title: 'Funzione RWByteAddressBuffer:: Load4 (uint)'
description: 'Ottiene quattro valori. | Funzione RWByteAddressBuffer:: Load4 (uint)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
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
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982049"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>Funzione RWByteAddressBuffer:: Load4 (uint)

Ottiene quattro valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Indirizzo* \[ in\]
</dt> <dd>

Tipo: **uint**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint4**

Quattro valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




