---
title: Funzione OutputPatch::Operator
description: Restituisce l'eesimo punto di controllo nella patch. | Funzione OutputPatch::Operator
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
keywords:
- Funzione operatore HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 684925491ce7b5ac50cb293b3c8a0270557c9b9e65fcfcde63e9699127bc7ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023471"
---
# <a name="outputpatchoperator--function"></a>Funzione OutputPatch::Operator

Restituisce *l'eesimo*<sup></sup> punto di controllo nella patch.

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

N *punto*<sup>di</sup> controllo.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




