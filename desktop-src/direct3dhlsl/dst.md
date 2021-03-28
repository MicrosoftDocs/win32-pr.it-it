---
title: funzione DST
description: Calcola un vettore di distanza. | funzione DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- funzione DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886090"
---
# <a name="dst-function"></a>funzione DST

Calcola un vettore di distanza.

## <a name="syntax"></a>Sintassi

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*src0* \[ in\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Primo vettore.

</dd> <dt>

*src1* \[ in\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Secondo vettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Vettore di distanza calcolato.

## <a name="remarks"></a>Commenti

Questa funzione intrinseca fornisce la stessa funzionalità dell'istruzione vertex shader dell'istruzione [DST](dst---vs.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




