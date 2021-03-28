---
title: 'Funzione ByteAddressBuffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione ByteAddressBuffer:: GetDimensions'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995293"
---
# <a name="byteaddressbuffergetdimensions-function"></a>Funzione ByteAddressBuffer:: GetDimensions

Ottiene la lunghezza del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Dim* \[ out\]
</dt> <dd>

Tipo: **uint**

Lunghezza, in byte, del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ByteAddressBuffer](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




