---
title: Funzione RWStructuredBuffer::GetDimensions
description: Ottiene le dimensioni della risorsa. | Funzione RWStructuredBuffer::GetDimensions
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 760a546d7d60afbb41438416a9602ab55981834acd9969bc535c9a82df6e5e50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789927"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>Funzione RWStructuredBuffer::GetDimensions

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

Numero di strutture nella risorsa.

</dd> <dt>

*stride* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stride, in byte, di ogni elemento della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




