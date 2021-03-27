---
title: 'Funzione buffer:: GetDimensions'
description: 'Ottiene la lunghezza del buffer. | Funzione buffer:: GetDimensions'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981090"
---
# <a name="buffergetdimensions-function"></a>Funzione buffer:: GetDimensions

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

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




