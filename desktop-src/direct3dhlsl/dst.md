---
title: Funzione dst
description: Calcola un vettore di distanza. | Funzione dst
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- Funzione dst HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068341"
---
# <a name="dst-function"></a>Funzione dst

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

*src0* \[ Pollici\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Primo vettore.

</dd> <dt>

*src1* \[ Pollici\]
</dt> <dd>

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Secondo vettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[fVector](dx-graphics-hlsl-vector.md)**

Vettore di distanza calcolato.

## <a name="remarks"></a>Commenti

Questa funzione intrinseca fornisce la stessa funzionalità dell'istruzione Vertex Shader [dst](dst---vs.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




