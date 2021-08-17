---
title: Funzione RWByteAddressBuffer::InterlockedMin
description: Trova il valore minimo in modo atomico.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Funzione InterlockedMin HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 062ae6c5fa37b732411891427770761881429069d030e9266ab20adb3e2d3726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509550"
---
# <a name="interlockedmin-function"></a>Funzione InterlockedMin

Trova il valore minimo in modo atomico.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedMin(
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

*valore \_ originale* \[ in uscita\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse di tipo int e uint e variabili di memoria condivisa. Questa funzione può essere utilizzata in tre modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un minimo atomico del valore nel registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un minimo atomico del valore nella posizione della risorsa a cui fa riferimento dest. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce al minimo il valore di dest e value, archiviato in dest. La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

Questa funzione è supportata nei tipi di shader seguenti:



| VS  | Hs  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 