---
title: 'Funzione RWByteAddressBuffer:: InterlockedCompareStore'
description: Ccompares l'input al valore di confronto in modo atomico.
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
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872786"
---
# <a name="interlockedcomparestore-function"></a>InterlockedCompareStore (funzione)

Ccompares l'input al valore di confronto in modo atomico.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*dest* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indirizzo di destinazione.

</dd> <dt>

*Confronta \_ valore* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valore di confronto.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione può essere eseguita solo su risorse tipizzate int o uint e variabili di memoria condivisa. Per questa funzione sono disponibili tre possibili utilizzi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento dest. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento dest. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce l'operazione eseguita usando le operazioni locali.

Questa funzione è supportata nei tipi di shader seguenti:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 