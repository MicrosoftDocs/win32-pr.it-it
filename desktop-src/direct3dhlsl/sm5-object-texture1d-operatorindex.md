---
title: Funzione Texture1D::Operator
description: Restituisce una variabile di risorsa di sola lettura per un oggetto Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: d2c11ef313531adb9b129ffb99103ea6c7778462eddf8c1c76f4b235c92951c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985911"
---
# <a name="texture1doperator--function"></a>Funzione Texture1D::Operator

Restituisce una variabile di risorsa di sola lettura per [**un oggetto Texture1D.**](sm5-object-texture1d.md)

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Posizione dell'indice. Contiene la coordinata x.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

Questo metodo accede sempre al primo livello mip. Per specificare altri livelli mip, usare [**invece \[ \] \[ \] mip.operator.**](sm5-object-texture1d-mipsoperatorindex.md)

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




