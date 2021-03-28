---
title: 'Funzione RWTexture1DArray:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture1DArray:: operator'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981711"
---
# <a name="rwtexture1darrayoperator--function"></a>Funzione RWTexture1DArray:: operator

Restituisce una variabile di risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ in\]
</dt> <dd>

Tipo: **uint2**

Posizione dell'indice. Il primo componente contiene la coordinata x. Il secondo componente indica la sezione della matrice desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




