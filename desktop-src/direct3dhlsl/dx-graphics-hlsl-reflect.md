---
title: Riflettere
description: Restituisce un vettore di reflection usando un raggio dell'evento imprevisto e una normale della superficie.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- reflect HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2abc7100eae846fc3d2f21b013676aa3dbc64574a7e8cdb8a14dc492ceb33f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725945"
---
# <a name="reflect"></a>Riflettere

Restituisce un vettore di reflection usando un raggio dell'evento imprevisto e una normale della superficie.



| *ret* reflect(*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Ho*<br/> | \[in \] un vettore di eventi imprevisti a virgola mobile.<br/> |
| <span id="n"></span><span id="N"></span>*N*<br/> | \[in \] un vettore normale a virgola mobile.<br/>   |



 

## <a name="return-value"></a>Valore restituito

Vettore di reflection a virgola mobile.

## <a name="remarks"></a>Commenti

Questa funzione calcola il vettore di reflection usando la formula seguente: v = i - 2 \* n \* punto(i n) .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *i* |
| *Ret* | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *i* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader superiori | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

