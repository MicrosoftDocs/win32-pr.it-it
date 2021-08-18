---
title: Illuminato
description: Restituisce un vettore del coefficiente di illuminazione.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- lit HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791626"
---
# <a name="lit"></a>Illuminato

Restituisce un vettore del coefficiente di illuminazione.



| *ret* lit(*n \_ dot \_ l*, *n dot \_ \_ h*, *m*) |
|------------------------------------------|



 

Questa funzione restituisce un vettore del coefficiente di illuminazione (ambiente, diffusione, speculare, 1) in cui:

-   ambiente = 1
-   diffuse = n · l < 0 ? 0 : n · L
-   specular = n · l < 0 \| \| n · h < 0 ? 0 : (n · h) ^ m

Dove il vettore n è il vettore normale, l è la direzione verso la luce e h è il mezzo vettore.

## <a name="parameters"></a>Parametri



| Elemento                                                                       | Descrizione                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*<br/> | \[in \] Prodotto del punto della normale della superficie normalizzata e del vettore di luce.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ dot \_ h*<br/> | \[in \] Prodotto del punto del vettore a mezzo angolo e della normale della superficie.<br/>       |
| <span id="m"></span><span id="M"></span>*M*<br/>                     | \[in \] Esponente speculare.<br/>                                                   |



 

## <a name="return-value"></a>Valore restituito

Vettore del coefficiente di illuminazione.

## <a name="type-description"></a>Descrizione del tipo



| Nome        | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ punto \_ l* | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ dot \_ h* | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Ret*       | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | sì (solo \_ vs 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

