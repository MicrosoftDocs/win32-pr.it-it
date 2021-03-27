---
title: 'Funzione RWByteAddressBuffer:: InterlockedCompareExchange'
description: Confronta l'input con il valore di confronto e scambia il risultato in modo atomico.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Funzione InterlockedCompareExchange HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729143"
---
# <a name="interlockedcompareexchange-function"></a>InterlockedCompareExchange (funzione)

Confronta l'input con il valore di confronto e scambia il risultato in modo atomico.

## <a name="syntax"></a>Sintassi

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
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

*Confronta \_ valore* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valore di confronto.

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

Confronta in modo atomico il valore in *dest* per *confrontare \_ value*, archivia il valore in *dest* se i valori corrispondono, restituisce il valore originale di *dest* nel *\_ valore originale*. Questa operazione può essere eseguita solo su risorse tipizzate **int** o *uint* e variabili di memoria condivisa. Per questa funzione sono disponibili tre possibili utilizzi. Il primo è quando R è un tipo di variabile di memoria condivisa. In questo caso, la funzione esegue l'operazione sul Registro di memoria condiviso a cui fa riferimento *dest*. Il secondo scenario è quando R è un tipo di variabile di risorsa. In questo scenario, la funzione esegue l'operazione sul percorso della risorsa a cui fa riferimento *dest*. Infine, il terzo scenario è quando R è un tipo di variabile locale. In questo scenario, la funzione riduce l'operazione eseguita usando le operazioni locali. Questa operazione è disponibile solo se R è leggibile e scrivibile.

> [!Note]  
> Se si chiama **InterlockedCompareExchange** in un ciclo [**for**](dx-graphics-hlsl-for.md) o [**while**](dx-graphics-hlsl-while.md) compute shader, per la corretta compilazione è necessario usare l'attributo **\[ allow \_ \_ Condition \] UAV** in quel ciclo.

 

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

 

 