---
title: 'Funzione RWByteAddressBuffer:: InterlockedAnd'
description: Il valore, in modo atomico.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- Funzione InterlockedAnd HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399206"
---
# <a name="interlockedand-function"></a>InterlockedAnd (funzione)

Il valore, in modo atomico.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indirizzo di destinazione.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> <dt>

*\_ valore originale* in \[ uscita\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa. Per questa funzione sono disponibili tre possibili utilizzi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue un'operazione atomica e di valore nel registro di memoria condiviso a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue un'operazione atomica e di valore nel percorso della risorsa a cui fa riferimento dest. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce a e del valore di dest e value, archiviati in dest. La funzione in overload ha una variabile di output aggiuntiva che verrà impostata sul valore originale di dest. Questa operazione di overload è disponibile solo quando R è leggibile e scrivibile.

Questa funzione è supportata nei tipi di shader seguenti:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   |  x  | x   | x   | x   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 