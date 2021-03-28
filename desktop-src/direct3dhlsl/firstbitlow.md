---
title: firstbitlow (funzione)
description: Restituisce la posizione del primo bit impostato a partire dal bit di ordine più basso e procedendo verso l'alto, per componente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- Funzione firstbitlow HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046937"
---
# <a name="firstbitlow-function"></a>firstbitlow (funzione)

Restituisce la posizione del primo bit impostato a partire dal bit di ordine più basso e procedendo verso l'alto, per componente.

## <a name="syntax"></a>Sintassi

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di in\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Posizione del primo bit impostato.

## <a name="remarks"></a>Commenti

Sono disponibili anche le seguenti versioni di overload:

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 