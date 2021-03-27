---
title: acceso
description: Restituisce un vettore di coefficienti di illuminazione.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL illuminato
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872541"
---
# <a name="lit"></a>acceso

Restituisce un vettore di coefficienti di illuminazione.



| *ret* lit (*n \_ punto \_ l*, *n \_ punto \_ h*, *m*) |
|------------------------------------------|



 

Questa funzione restituisce un vettore di coefficienti di illuminazione (ambiente, diffuso, speculare, 1) in cui:

-   ambiente = 1
-   diffusa = n · l < 0? 0: n · l
-   speculare = n · l < 0 \| \| n · h < 0? 0: (n · h) ^ m

Dove Vector n è il vettore normale, l è la direzione della luce e h è il vettore mezzo.

## <a name="parameters"></a>Parametri



| Elemento                                                                       | Descrizione                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*<br/> | \[nel \] prodotto a punti della superficie normalizzata normale e del vettore chiaro.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*<br/> | \[nel \] prodotto a virgola del vettore a metà angolo e della normale della superficie.<br/>       |
| <span id="m"></span><span id="M"></span>*m*<br/>                     | \[in \] un esponente speculare.<br/>                                                   |



 

## <a name="return-value"></a>Valore restituito

Vettore di coefficiente di illuminazione.

## <a name="type-description"></a>Descrizione del tipo



| Nome        | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ punto \_ l* | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ punto \_ h* | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *RET*       | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

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

 

