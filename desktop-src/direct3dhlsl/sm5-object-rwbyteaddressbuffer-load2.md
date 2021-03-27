---
title: 'Funzione RWByteAddressBuffer:: load2 (uint)'
description: 'Ottiene due valori. | Funzione RWByteAddressBuffer:: load2 (uint)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Funzione load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982028"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>Funzione RWByteAddressBuffer:: load2 (uint)

Ottiene due valori.

## <a name="syntax"></a>Sintassi

``` syntax
uint2 Load2(
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

Tipo: **uint2**

Due valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi load2](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




