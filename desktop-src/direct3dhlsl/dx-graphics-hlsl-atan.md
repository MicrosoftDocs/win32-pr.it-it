---
title: atan
description: Restituisce l'arcotangente del valore specificato.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- atan HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69c3b51381318627dd5c3ce7b64fe405968c669418bdf743b5c56eaae535b0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726401"
---
# <a name="atan"></a>atan

Restituisce l'arcotangente del valore specificato.



| *ret* atan(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Arcotangente del *parametro x.* Questo valore è compreso nell'intervallo da -π/2 a π/2.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì       |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

