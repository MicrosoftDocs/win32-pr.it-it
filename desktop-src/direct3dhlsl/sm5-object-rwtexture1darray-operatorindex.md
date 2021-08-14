---
title: Funzione RWTexture1DArray::Operator
description: Restituisce una variabile di risorsa. | Funzione RWTexture1DArray::Operator
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 2e0735e3d9945d15c2f8473155612a40cbf652349eb531f089f5a4aa44451484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509283"
---
# <a name="rwtexture1darrayoperator--function"></a>Funzione RWTexture1DArray::Operator

Restituisce una variabile di risorsa.

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

Posizione dell'indice. Il primo componente contiene la coordinata x. Il secondo componente indica la sezione di matrice desiderata.

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

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




