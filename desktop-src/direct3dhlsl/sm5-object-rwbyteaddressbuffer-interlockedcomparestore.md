---
title: Funzione RWByteAddressBuffer::InterlockedCompareStore
description: Ccompare l'input al valore di confronto, in modo atomico.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- Funzione InterlockedCompareStore HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb19358f98c1280ddb180b7381fb7714d28cc7db145ca36577f5f97f70c9f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509690"
---
# <a name="interlockedcomparestore-function"></a>Funzione InterlockedCompareStore

Ccompare l'input al valore di confronto, in modo atomico.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indirizzo di destinazione.

</dd> <dt>

*confrontare \_ il valore* \[ in\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valore di confronto.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipiche int o uint e variabili di memoria condivisa. Esistono tre possibili utilizzi per questa funzione. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul registro di memoria condivisa a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione si riduce all'operazione eseguita usando operazioni locali.

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

 

 