---
title: SmoothStep
description: Restituisce un'interpolazione dell'eremita smussata tra 0 e 1, se x è compreso nell'intervallo \ min, max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL SmoothStep
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976671"
---
# <a name="smoothstep"></a>SmoothStep

Restituisce un'interpolazione dell'eremita smussata tra 0 e 1, se *x* è compreso nell'intervallo \[ *min*, *Max* \] .



| SmoothStep *ret* (*min*, *Max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[nell' \] intervallo minimo del parametro *x* .<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[nell' \] intervallo massimo del parametro *x* .<br/> |
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[nel \] valore specificato da interpolare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Restituisce 0 se *x* è minore di *min*; 1 se *x* è maggiore di *Max*; in caso contrario, un valore compreso tra 0 e 1 se *x* è compreso nell'intervallo \[ *min*, *Max* \] .

## <a name="remarks"></a>Commenti

Usare la funzione intrinseca **SmoothStep** HLSL per creare una transizione uniforme tra due valori. Ad esempio, è possibile usare questa funzione per unire due colori in modo uniforme.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |
| *max* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sì ( \_ solo vs 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

