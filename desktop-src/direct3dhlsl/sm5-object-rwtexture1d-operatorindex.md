---
title: 'Funzione RWTexture1D:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWTexture1D:: operator'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530613"
---
# <a name="rwtexture1doperator--function"></a>Funzione RWTexture1D:: operator

Restituisce una variabile di risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* \[ in\]
</dt> <dd>

Tipo: **uint**

Posizione dell'indice. Contiene la coordinata x.

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

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




