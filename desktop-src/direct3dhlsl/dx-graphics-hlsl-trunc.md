---
title: tronca (Corecrt \_ Math. h)
description: Tronca un valore a virgola mobile nel componente intero.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- tronca HLSL
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
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995945"
---
# <a name="trunc"></a>trunc

Tronca un valore a virgola mobile nel componente intero.



| troncamento RET (*x*) |
|----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nell' \] input specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore di input troncato a un componente intero.

## <a name="remarks"></a>Commenti

Questa funzione tronca un valore a virgola mobile nel componente intero. Dato un valore a virgola mobile 1,6, la funzione tronca restituirà 1,0, dove la funzione [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) restituirà 2,0.

## <a name="type-description"></a>Descrizione del tipo



| Nome | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| RET  | Stesso tipo di input x                                                                                           | [**float**](/windows/desktop/WinProg/windows-data-types)                        | Le stesse dimensioni di input x |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati | sì       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

