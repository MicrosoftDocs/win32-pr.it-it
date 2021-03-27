---
title: 'Funzione Texture2DMSArray:: GetSamplePosition'
description: "Ottiene la posizione dell'esempio specificato. | Funzione Texture2DMSArray:: GetSamplePosition"
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234884"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Funzione Texture2DMSArray:: GetSamplePosition

Ottiene la posizione dell'esempio specificato.

## <a name="syntax"></a>Sintassi

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*sampleindex* \[ in\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero di una posizione di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **float2**

Percorso di esempio.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
