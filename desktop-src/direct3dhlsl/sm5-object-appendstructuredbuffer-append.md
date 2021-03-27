---
title: 'Funzione AppendStructuredBuffer:: Append'
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
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103956033"
---
# <a name="append-function"></a>Append (funzione)

Aggiunge un valore alla fine del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **T**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

T può essere qualsiasi tipo di dati, incluse le strutture.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




