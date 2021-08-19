---
title: Funzione AppendStructuredBuffer::Append
description: Aggiunge un valore alla fine del buffer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Funzione Append HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725395"
---
# <a name="append-function"></a>Funzione Append

Aggiunge un valore alla fine del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

T può essere qualsiasi tipo di dati, incluse le strutture.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




