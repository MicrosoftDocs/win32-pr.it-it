---
title: Determinante
description: Restituisce il determinante della matrice quadrata a virgola mobile specificata.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- determinant HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b17982560d70cf00cfb13832de9605b910f169d1461692f4c6a97274709e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120306"
---
# <a name="determinant"></a>Determinante

Restituisce il determinante della matrice quadrata a virgola mobile specificata.



| *ret* determinant(*m*) |
|------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*M*<br/> | \[in \] Valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore scalare a virgola mobile che rappresenta il determinante del *parametro m.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**Matrice**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any (numero di righe = numero di colonne) |
| *Ret* | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                   |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

