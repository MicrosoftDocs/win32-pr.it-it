---
title: 'Funzione ConsumeStructuredBuffer:: consume'
description: Rimuove un valore dalla fine del buffer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Usa funzione HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045987"
---
# <a name="consume-function"></a>Funzione consume

Rimuove un valore dalla fine del buffer.

## <a name="syntax"></a>Sintassi

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **T**

Il valore è stato rimosso (può essere una struttura).

## <a name="remarks"></a>Commenti

T può essere qualsiasi tipo di dati, inclusa una struttura.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




