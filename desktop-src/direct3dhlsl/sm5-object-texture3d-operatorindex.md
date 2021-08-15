---
title: Funzione Texture3D::Operator
description: Restituisce una variabile di risorsa di sola lettura. | Funzione Texture3D::Operator
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: d701e5f9ba46d17c305fda0a936700e10a1348440e55c913537f2a2d00a5c57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985701"
---
# <a name="texture3doperator--function"></a>Funzione Texture3D::Operator

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ Pollici\]
</dt> <dd>

Tipo: **uint3**

Posizione dell'indice. Contiene le coordinate (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

Questo metodo accede sempre al primo livello mip. Per specificare altri livelli mip, usare [**invece \[ \] \[ \] mip.operator.**](sm5-object-texture3d-mipsoperatorindex.md)

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




