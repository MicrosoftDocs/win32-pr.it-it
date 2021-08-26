---
title: trunc (Corecrt \_ math.h)
description: Tronca un valore a virgola mobile nel componente integer.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0845e619e8674d729735da1b639802df256d9c210615d71578a4e1effd777e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845771"
---
# <a name="trunc"></a>trunc

Tronca un valore a virgola mobile nel componente integer.



| ret trunc(*x*) |
|----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Input specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore di input troncato in un componente integer.

## <a name="remarks"></a>Commenti

Questa funzione tronca un valore a virgola mobile al componente integer. Dato un valore a virgola mobile 1,6, la funzione trunc restituirebbe 1.0, dove come funzione round [**(DirectX HLSL)**](dx-graphics-hlsl-round.md) restituirebbe 2.0.

## <a name="type-description"></a>Descrizione del tipo



| Nome | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| Ret  | Stesso tipo dell'input x                                                                                           | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | Stesse dimensioni dell'input x |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader superiori | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

