---
title: 'Funzione RWByteAddressBuffer:: Load3 (uint)'
description: 'Ottiene tre valori. | Funzione RWByteAddressBuffer:: Load3 (uint)'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Funzione Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982058"
---
# <a name="rwbyteaddressbufferload3uint-function"></a>Funzione RWByteAddressBuffer:: Load3 (uint)

Ottiene tre valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint3 Load3(
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

Tipo: **uint3**

Tre valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load3](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




