---
title: refract
description: Restituisce un vettore di refrazione usando un raggio di ingresso, una normale della superficie e un indice di refrazione.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- refract HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3895f39d7559fbc8707d3306d8183bfcef60890fa0393a788d17822137b8de2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090978"
---
# <a name="refract"></a>refract

Restituisce un vettore di refrazione usando un raggio di ingresso, una normale della superficie e un indice di refrazione.



| *ret* refract(*i*, *n*, ?) |
|----------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Ho*<br/> | \[in \] Un vettore di direzione del raggio a virgola mobile.<br/>    |
| <span id="n"></span><span id="N"></span>*N*<br/> | \[in \] un vettore normale della superficie a virgola mobile.<br/>   |
| *?*<br/>                                         | \[in \] un indice a virgola mobile a virgola mobile scalare dell'indice di refrazione.<br/> |



 

## <a name="return-value"></a>Valore restituito

Vettore di rifrazione a virgola mobile. Se l'angolo tra il raggio di ingresso i e la normale della superficie n è troppo grande per un determinato indice di refrazione ?, il valore restituito è (0,0,0).

## <a name="type-description"></a>Descrizione del tipo



| Nome              | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*               | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *i* |
| ?                 | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| vettore di refrazione | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *i* |



 

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

 

