---
title: 'Funzione Texture2DMS:: GetSamplePosition'
description: Restituisce la posizione di esempio per l'indice di esempio fornito.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
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
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517325"
---
# <a name="texture2dmsgetsampleposition-function"></a>Funzione Texture2DMS:: GetSamplePosition

Restituisce la posizione di esempio per l'indice di esempio fornito.

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
