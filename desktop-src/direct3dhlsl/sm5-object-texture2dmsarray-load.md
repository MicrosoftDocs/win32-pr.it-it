---
title: 'Funzione Texture2DMSArray:: Load (int, int)'
description: 'Ottiene un valore. | Funzione Texture2DMSArray:: Load (int, int)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969249"
---
# <a name="texture2dmsarrayloadintint-function"></a>Funzione Texture2DMSArray:: Load (int, int)

Ottiene un valore.

## <a name="syntax"></a>Sintassi

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Coord* \[ in\]
</dt> <dd>

Tipo: **INT3**

Percorso di input.

</dd> <dt>

*sampleindex* \[ in\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Indice di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **T**

Un valore il cui tipo corrisponde al tipo di modello di trama.

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load](texture2dmsarray-load.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
