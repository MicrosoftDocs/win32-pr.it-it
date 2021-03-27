---
title: morsetto
description: Consente di bloccare il valore specificato nell'intervallo minimo e massimo specificato.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- blocca HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729543"
---
# <a name="clamp"></a>morsetto

Consente di bloccare il valore specificato nell'intervallo minimo e massimo specificato.



| morsetto *ret* (*x*, *min*, *Max*) |
|--------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[in \] un valore da bloccare.<br/>            |
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[nell' \] intervallo minimo specificato.<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[nell' \] intervallo massimo specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore premuto per il parametro *x* .

## <a name="remarks"></a>Commenti

Per i valori di-INF o INF, il morsetto si comporterà come previsto. Per i valori NaN, tuttavia, i risultati non sono definiti.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *min* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | le stesse dimensioni di input *x* |
| *max* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | le stesse dimensioni di input *x* |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

