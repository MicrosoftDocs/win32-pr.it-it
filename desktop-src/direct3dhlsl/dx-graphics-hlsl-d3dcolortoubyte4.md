---
title: D3DCOLORtoUBYTE4
description: Converte un vettore 4D a virgola mobile impostato da un D3DCOLOR in un UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- HLSL D3DCOLORtoUBYTE4
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517073"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Converte un vettore 4D a virgola mobile impostato da un D3DCOLOR in un UBYTE4.



| *ret* D3DCOLORtoUBYTE4 (*x*) |
|-----------------------------|



 

Questa funzione swizzles e ridimensiona i componenti del parametro *x* . Usare questa funzione per compensare la mancanza di supporto UBYTE4 in alcuni componenti hardware.

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nell' \] oggetto Vector4 a virgola mobile da convertire.<br/> |



 

## <a name="return-value"></a>Valore restituito

Rappresentazione UBYTE4 del parametro *x* .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *RET* | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**intero**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

