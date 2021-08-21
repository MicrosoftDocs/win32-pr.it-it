---
title: smoothstep
description: Restituisce un'interpolazione ermete uniforme tra 0 e 1, se x è compreso nell'intervallo \ min, max\ .
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- Smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5416dab57fc77f7b664518afcb0f4623875fd2a660f7d1aff82ab42f2c297b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513797"
---
# <a name="smoothstep"></a>smoothstep

Restituisce un'interpolazione ermete uniforme tra 0 e 1, se *x* è compreso nell'intervallo \[ *min*, *max* \] .



| *ret* smoothstep(*min*, *max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*Minimo*<br/> | \[in \] Intervallo minimo del parametro *x.*<br/> |
| <span id="max"></span><span id="MAX"></span>*Massimo*<br/> | \[in \] Intervallo massimo del parametro *x.*<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[in \] Valore specificato da interpolare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Restituisce 0 se *x* è minore di *min*; 1 se *x* è maggiore di *max*; in caso contrario, un valore compreso tra 0 e 1 se *x* è compreso nell'intervallo \[ *min*, *max* \] .

## <a name="remarks"></a>Commenti

Usare la **funzione intrinseca smoothstep** HLSL per creare una transizione uniforme tra due valori. Ad esempio, è possibile usare questa funzione per unire due colori senza problemi.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *max* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sì (solo vs \_ \_ 1 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

