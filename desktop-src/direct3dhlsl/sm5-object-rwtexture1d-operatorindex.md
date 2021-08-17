---
title: Funzione RWTexture1D::Operator
description: Restituisce una variabile di risorsa. | Funzione RWTexture1D::Operator
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: a6f338efd27573a86c661df36f9fc0e9906814bf15c1cc5d2d6c478a17f83a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724852"
---
# <a name="rwtexture1doperator--function"></a>Funzione RWTexture1D::Operator

Restituisce una variabile di risorsa.

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

Variabile di risorsa.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




