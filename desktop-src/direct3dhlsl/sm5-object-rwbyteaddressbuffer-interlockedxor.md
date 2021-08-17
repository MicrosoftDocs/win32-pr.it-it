---
title: Funzione RWByteAddressBuffer::InterlockedXor
description: Esegue un XOR atomico sul valore.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- Funzione InterlockedXor HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b9e0c719bb72116ba84a33f46c81cf243773d4c66e5ff0997066e7228b19db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905798"
---
# <a name="interlockedxor-function"></a>Funzione InterlockedXor

Esegue un **XOR atomico** sul valore.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedXor(
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

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su **risorse di** tipo INT o **UINT** e variabili di memoria condivisa. Questa funzione può essere utilizzata in tre modi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un **XOR** atomico con il valore del registro di memoria condivisa a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario la funzione esegue un **XOR** atomico con il valore della posizione della risorsa a cui fa riferimento *dest*. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce a **un XOR** dei valori *di dest* e *value*. Il risultato dell'operazione sostituisce il valore in *dest*. La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale *di dest*. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

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

 

 