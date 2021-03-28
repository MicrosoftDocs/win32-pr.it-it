---
title: 'Funzione RWByteAddressBuffer:: Archivio2'
description: Imposta due valori.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Funzione Archivio2 HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045984"
---
# <a name="store2-function"></a>Archivio2 (funzione)

Imposta due valori.

## <a name="syntax"></a>Sintassi

``` syntax
void Store2(
  in uint address,
  in uint2 values
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

Tipo: **uint2**

Due valori di input.

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

 

 




