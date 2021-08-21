---
title: larghezza di banda
description: Restituisce il valore assoluto dei derivati parziali del valore specificato.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- fwidth HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: feee9a017664e71c9c96f19fda5106870c04b947dc2b668e67f376626f7ea38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120175"
---
# <a name="fwidth"></a>larghezza di banda

Restituisce il valore assoluto dei derivati parziali del valore specificato.



| *ret* fwidth(*x*) |
|-------------------|



 

Questa funzione calcola quanto segue: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).

Questa funzione è supportata solo nei pixel shader.

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore assoluto dei derivati parziali del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader superiori | sì                 |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | yes (solo ps \_ 2 \_ x) |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | no                  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

