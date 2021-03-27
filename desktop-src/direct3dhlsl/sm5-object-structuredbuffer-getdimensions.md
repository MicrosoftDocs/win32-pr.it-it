---
title: 'Funzione StructuredBuffer:: GetDimensions'
description: 'Ottiene le dimensioni della risorsa. | Funzione StructuredBuffer:: GetDimensions'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352961"
---
# <a name="structuredbuffergetdimensions-function"></a>Funzione StructuredBuffer:: GetDimensions

Ottiene le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*numStructs* \[ out\]
</dt> <dd>

Tipo: **uint**

Numero di strutture nella risorsa.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Tipo: **uint**

Stride, in byte, di ogni elemento della struttura.

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

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




