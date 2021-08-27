---
title: Funzione Texture2D::Operator
description: Restituisce una variabile di risorsa di sola lettura. | Funzione Texture2D::Operator
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 99323f1dcf212fc42c413a4be8231aa22acbd00cf3f40b408e3f9f5eca59f578
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095071"
---
# <a name="texture2doperator--function"></a>Funzione Texture2D::Operator

Restituisce una variabile di risorsa di sola lettura.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ Pollici\]
</dt> <dd>

Tipo: **uint2**

Posizione dell'indice. Contiene le coordinate (x, y).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di risorsa di sola lettura.

## <a name="remarks"></a>Commenti

Questo metodo accede sempre al primo livello mip. Per specificare altri livelli mip, usare invece il [**metodo \[ \] \[ \] mip.operator.**](sm5-object-texture2d-mipsoperatorindex.md)

I campioni di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




