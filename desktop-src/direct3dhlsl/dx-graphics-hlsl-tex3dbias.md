---
title: tex3Dbias
description: Campionamento di una trama 3D dopo la distorsione del livello mip di t.w.
ms.assetid: 6a506036-90d1-420c-a712-a373068c8c16
keywords:
- tex3Dbias HLSL
topic_type:
- apiref
api_name:
- tex3Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1565f5290955e2fa5aceffd368e0abcbcb99cb4c0035e44db4e8ea6585a170c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892621"
---
# <a name="tex3dbias"></a>tex3Dbias

Campionamento di una trama 3D dopo la distorsione del livello mip di t.w.



| ret tex3Dbias(s, t) |
|---------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[nello \] stato del campionatore.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Coordinata trama.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati di trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | in uscita    | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato               |
|-----------------------------------------------------------|-------------------------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì (solo pixel shader) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sì (solo pixel shader) |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sì (solo pixel shader) |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                      |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

