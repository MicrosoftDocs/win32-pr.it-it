---
title: Funzione InputPatch::Operator
description: Restituisce l'eesimo punto di controllo nella patch. | Funzione InputPatch::Operator
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986031"
---
# <a name="inputpatchoperator--function"></a>Funzione InputPatch::Operator

Restituisce <sup>l'eesimo</sup> punto di controllo nella patch.

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

Punto di <sup>controllo</sup> *n.*

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




