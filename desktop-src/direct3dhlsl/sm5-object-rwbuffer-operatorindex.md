---
title: 'Funzione RWBuffer:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWBuffer:: operator'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995309"
---
# <a name="rwbufferoperator--function"></a>Funzione RWBuffer:: operator

Restituisce una variabile di risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ in\]
</dt> <dd>

Tipo: **uint**

Posizione dell'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




