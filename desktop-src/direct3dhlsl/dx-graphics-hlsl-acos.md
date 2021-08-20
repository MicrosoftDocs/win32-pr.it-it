---
title: acos
description: Restituisce l'arcocoseno del valore specificato.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- acos HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 155915f1a9163b8569b9c92a396161659df2addfc7e27f2acde8f05bf49808d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673611"
---
# <a name="acos"></a>acos

Restituisce l'arcocoseno del valore specificato.



| *ret* acos(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Il valore specificato. Ogni componente deve essere un valore a virgola mobile compreso nell'intervallo compreso tra -1 e 1.<br/> |



 

## <a name="return-value"></a>Valore restituito

Arcocoseno del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato     |
|------------------------------------------------------------------------------------|---------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì           |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | solo rispetto \_ a \_ 1 1 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

