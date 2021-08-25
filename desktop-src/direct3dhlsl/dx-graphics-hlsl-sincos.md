---
title: Sincos
description: Restituisce il seno e il coseno di x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- sincos HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff2854ea4c8b956298a65107136a963c5591b91de32d108b3179772bd0043a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673481"
---
# <a name="sincos"></a>Sincos

Restituisce il seno e il coseno di x.



| sincos(*x*, out *s*, out *c*) |
|-------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore specificato, espresso in radianti.<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/> | \[out \] Restituisce il seno di x.<br/>          |
| <span id="c"></span><span id="C"></span>*C*<br/> | \[out \] Restituisce il coseno di x.<br/>        |



 

## <a name="return-value"></a>Valore restituito

Nessuno.

## <a name="type-description"></a>Descrizione del tipo



| Nome | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*  | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *s*  | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| c    | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sì (solo vs \_ \_ 1 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

