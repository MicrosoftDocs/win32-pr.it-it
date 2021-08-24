---
title: faceforward
description: Capovolge la superficie normale (se necessario) per il viso in una direzione opposta a i; restituisce il risultato in n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- Faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 253d581ef5ea2eddac55c63245039f1ccda6c0e73032468d1598fb919e850a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950381"
---
# <a name="faceforward"></a>faceforward

Capovolge la superficie normale (se necessario) per il viso in una direzione opposta a i; restituisce il risultato in n.



| *ret* faceforward(*n*, *i*, *ng*) |
|-----------------------------------|



 

Questa funzione usa la formula seguente: -*n*  sign(dot(*i*, *ng*)).

## <a name="parameters"></a>Parametri



| Elemento                                                      | Descrizione                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/>    | \[in \] Vettore normale della superficie a virgola mobile risultante.<br/>                                           |
| <span id="i"></span><span id="I"></span>*Ho*<br/>    | \[in \] Un vettore di eventi imprevisti a virgola mobile che punta dalla posizione di visualizzazione alla posizione dell'ombreggiatura.<br/> |
| <span id="ng"></span><span id="NG"></span>*Ng*<br/> | \[in \] Un vettore normale della superficie a virgola mobile.<br/>                                                       |



 

## <a name="return-value"></a>Valore restituito

Vettore normale della superficie a virgola mobile rivolto verso la direzione di visualizzazione.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *n* |
| *Ng*  | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *n*   |
| *Ret* | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *n*   |



 

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

 

