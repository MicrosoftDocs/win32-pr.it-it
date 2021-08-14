---
title: Funzione Texture2DMSArray::GetSamplePosition
description: Ottiene la posizione dell'esempio specificato. | Funzione Texture2DMSArray::GetSamplePosition
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- Funzione GetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508417"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Funzione Texture2DMSArray::GetSamplePosition

Ottiene la posizione dell'esempio specificato.

## <a name="syntax"></a>Sintassi

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*sampleindex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero di una posizione di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float2**

Posizione di esempio.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
