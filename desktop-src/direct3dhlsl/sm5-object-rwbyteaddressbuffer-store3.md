---
title: 'Funzione RWByteAddressBuffer:: Store3'
description: Imposta tre valori.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Funzione Store3 HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335087"
---
# <a name="store3-function"></a>Store3 (funzione)

Imposta tre valori.

## <a name="syntax"></a>Sintassi

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Indirizzo* \[ in\]
</dt> <dd>

Tipo: **uint**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> <dt>

*valori* \[ di in\]
</dt> <dd>

Tipo: **uint3**

Tre valori di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




