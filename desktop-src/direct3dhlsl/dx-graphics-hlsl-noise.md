---
title: rumore
description: Genera un valore casuale usando l'algoritmo Perlin-noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HLSL rumore
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399956"
---
# <a name="noise"></a>rumore

Genera un valore casuale usando l'algoritmo Perlin-noise.




| rumore *ret* (*x*) |
|------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[in \] un vettore a virgola mobile da cui generare il rumore Perlin.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore del rumore Perlin compreso in un intervallo compreso tra-1 e 1.

## <a name="remarks"></a>Commenti

I valori del rumore Perlin cambiano senza intoppi da un punto a un altro su uno spazio, creando valori generati in modo casuale e alla ricerca naturale. È possibile usare il rumore Perlin per generare trame procedurali per effetti quali fumo e incendi.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any  |
| *RET* | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | no                  |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sì ( \_ solo TX 1 \_ 0) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

