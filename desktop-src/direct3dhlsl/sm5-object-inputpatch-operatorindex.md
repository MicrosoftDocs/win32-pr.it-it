---
title: 'Funzione InputPatch:: operator'
description: "Restituisce l'ennesimo punto di controllo nella patch. | Funzione InputPatch:: operator"
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234722"
---
# <a name="inputpatchoperator--function"></a>Funzione InputPatch:: operator

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
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




