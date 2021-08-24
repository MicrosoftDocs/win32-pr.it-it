---
title: Funzione ByteAddressBuffer::Load(int)
description: Ottiene un valore. | Funzione ByteAddressBuffer::Load(int)
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Caricare la funzione HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a9854f85ebd92b9f57e4b2339f374ad8f7816ea7b9ba31e37c9404b08c14864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671451"
---
# <a name="byteaddressbufferloadint-function"></a>Funzione ByteAddressBuffer::Load(int)

Ottiene un valore.

## <a name="syntax"></a>Sintassi

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*address* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](byteaddressbuffer-load.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




