---
title: Funzione ConsumeStructuredBuffer::GetDimensions
description: Ottiene le dimensioni della risorsa. | Funzione ConsumeStructuredBuffer::GetDimensions
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: 5cc7c7c9234d00343f91a3fcb137eed65b95515a07f765cf8fce6893e2d4998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788391"
---
# <a name="consumestructuredbuffergetdimensions-function"></a>Funzione ConsumeStructuredBuffer::GetDimensions

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

*NumStructs* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Numero di strutture.

</dd> <dt>

*stride* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stride, in byte, di ogni elemento.

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

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




