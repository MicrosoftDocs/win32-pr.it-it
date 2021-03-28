---
title: faceforward
description: Capovolge la superficie normale, se necessario, in una direzione opposta a i; Restituisce il risultato in n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117934"
---
# <a name="faceforward"></a>faceforward

Capovolge la superficie normale, se necessario, in una direzione opposta a i; Restituisce il risultato in n.



| faceforward *ret* (*n*, *i*, *ng*) |
|-----------------------------------|



 

Questa funzione usa la formula seguente:-*n*  Sign (dot (*i*, *ng*)).

## <a name="parameters"></a>Parametri



| Elemento                                                      | Descrizione                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*n*<br/>    | \[nella \] superficie a virgola mobile risultante, vector normale.<br/>                                           |
| <span id="i"></span><span id="I"></span>*i*<br/>    | \[in \] un vettore di evento imprevisto a virgola mobile che punta dalla posizione di visualizzazione alla posizione di ombreggiatura.<br/> |
| <span id="ng"></span><span id="NG"></span>*ng*<br/> | \[in \] una superficie a virgola mobile-vettore normale.<br/>                                                       |



 

## <a name="return-value"></a>Valore restituito

Vettore normale della superficie A virgola mobile che si trova verso la direzione della visualizzazione.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *n* |
| *ng*  | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *n*   |
| *RET* | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *n*   |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

