---
title: 'Funzione Texture1DArray:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture1DArray:: operator'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981631"
---
# <a name="texture1darrayoperator--function"></a>Funzione Texture1DArray:: operator

Restituisce una variabile di risorsa di sola lettura.

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

Variabile di sola lettura di una risorsa.

## <a name="remarks"></a>Commenti

Questo metodo accede sempre al primo livello MIP. Per specificare altri livelli MIP, usare invece il metodo [**MIP \[ \] \[ \] . operator**](sm5-object-texture1darray-mipsoperatorindex.md) .

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




