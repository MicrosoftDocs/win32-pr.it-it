---
title: 'Funzione OutputPatch:: operator'
description: "Restituisce l'ennesimo punto di controllo nella patch. | Funzione OutputPatch:: operator"
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352711"
---
# <a name="outputpatchoperator--function"></a>Funzione OutputPatch:: operator

Restituisce il punto <sup>di controllo</sup> *n* nella patch.

## <a name="syntax"></a>Sintassi

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **uint**

Indice di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **T**

Il punto <sup>di controllo</sup> *n*.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




