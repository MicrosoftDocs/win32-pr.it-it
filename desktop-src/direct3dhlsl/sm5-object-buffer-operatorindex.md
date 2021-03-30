---
title: 'Funzione buffer:: operator'
description: 'Restituisce una variabile di risorsa di sola lettura. | Funzione buffer:: operator'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Scrittura diretta funzione operatore
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401852"
---
# <a name="bufferoperator--function"></a>Funzione buffer:: operator

Restituisce una variabile di risorsa di sola lettura.

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

Posizione dell'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **R**

Variabile di sola lettura di una risorsa.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




