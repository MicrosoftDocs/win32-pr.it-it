---
title: Funzione RWByteAddressBuffer::InterlockedMax
description: Trova il valore massimo, atomicamente.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Funzione InterlockedMax HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ca02966843d74aa17c3f5292ee3edf868140ae5722c26f47ec0270722cbbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790276"
---
# <a name="interlockedmax-function"></a>Funzione InterlockedMax

Trova il valore massimo, atomicamente.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indirizzo di destinazione.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> <dt>

*valore \_ originale* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipiche int e uint e variabili di memoria condivisa. Esistono tre possibili utilizzi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un massimo atomico del valore nel registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un massimo atomico del valore nel percorso della risorsa a cui fa riferimento dest. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce al massimo il valore di dest e value, archiviato in dest. La funzione di overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

Questa funzione è supportata nei tipi di shader seguenti:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 