---
title: 'Funzione Texture2DArray:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione Texture2DArray:: operator'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058500"
---
# <a name="texture2darrayoperator--function"></a>Funzione Texture2DArray:: operator

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ in\]
</dt> <dd>

Tipo: **uint3**

Posizione dell'indice. Il primo e il secondo componente contengono le coordinate (x, y). Il terzo componente indica la sezione della matrice desiderata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di sola lettura di una risorsa.

## <a name="remarks"></a>Commenti

Questo metodo accede sempre al primo livello MIP. Per specificare altri livelli MIP, usare invece il metodo [**MIP \[ \] \[ \] . operator**](sm5-object-texture2darray-mipsoperatorindex.md) .

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




