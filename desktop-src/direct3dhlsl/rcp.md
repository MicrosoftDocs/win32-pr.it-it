---
title: rcp
description: Calcola un reciproco rapido, approssimativo per componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- rcp HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb66fd2edf543dfb8beaf23dd2105925d15d169ee1b134019fb54da8fdf889e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672221"
---
# <a name="rcp"></a>rcp

Calcola un reciproco rapido, approssimativo per componente.



| *ret* rcp(*x*) |
|----------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

\[in \] Valore di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Reciproco del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                      | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types) o [ **double**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types) o [ **double**](/windows/desktop/WinProg/windows-data-types) | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 