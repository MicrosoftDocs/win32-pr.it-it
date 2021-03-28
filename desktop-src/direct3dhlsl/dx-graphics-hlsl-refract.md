---
title: rifrangono
description: Restituisce un vettore di rifrazione usando un raggio di immissione, una normale della superficie e un indice di rifrazione.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL di rifrazione
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993568"
---
# <a name="refract"></a>rifrangono

Restituisce un vettore di rifrazione usando un raggio di immissione, una normale della superficie e un indice di rifrazione.



| rifrazione *ret* (*i*, *n*,?) |
|----------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*i*<br/> | \[in \] un vettore a virgola mobile e direzione raggio.<br/>    |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[in \] un vettore a virgola mobile, superficie normale.<br/>   |
| *?*<br/>                                         | \[in \] una virgola mobile, indice rifrazione scalare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Vettore di rifrazione A virgola mobile. Se l'angolo tra il raggio i e la normale della superficie n è troppo grande per un indice di rifrazione specificato, il valore restituito è (0, 0, 0).

## <a name="type-description"></a>Descrizione del tipo



| Nome              | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*               | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *i* |
| ?                 | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| vettore di rifrazione | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *i* |



 

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

 

