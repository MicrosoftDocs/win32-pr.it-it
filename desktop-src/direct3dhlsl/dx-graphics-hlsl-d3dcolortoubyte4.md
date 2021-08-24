---
title: D3DCOLORtoUBYTE4
description: Converte un vettore 4D a virgola mobile impostato da D3DCOLOR in UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cea438b8c305c7ff76b6f9795c9f2c869a0f262f70e670d2e34c5b882de7c9c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789801"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Converte un vettore 4D a virgola mobile impostato da D3DCOLOR in UBYTE4.



| *ret* D3DCOLORtoUBYTE4(*x*) |
|-----------------------------|



 

Questa funzione scorre e ridimensiona i componenti del *parametro x.* Usare questa funzione per compensare la mancanza di supporto UBYTE4 in alcuni componenti hardware.

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Vettore a virgola mobile 4 da convertire.<br/> |



 

## <a name="return-value"></a>Valore restituito

Rappresentazione UBYTE4 del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *Ret* | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Intero**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì       |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

