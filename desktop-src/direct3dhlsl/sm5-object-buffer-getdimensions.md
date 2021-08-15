---
title: Funzione Buffer::GetDimensions
description: Ottiene la lunghezza del buffer. | Funzione Buffer::GetDimensions
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
ms.openlocfilehash: d7c56d673e533b4626a57669cf884d80da63d7848cfc7a3e248762f6c4f42088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986101"
---
# <a name="buffergetdimensions-function"></a>Funzione Buffer::GetDimensions

Ottiene la lunghezza del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

Tipo: **uint**

Lunghezza, in byte, del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




