---
description: Definisce un frame di coordinate o &\# 0034; frame di riferimento. &\# 0034; Il modello di frame è aperto e può contenere qualsiasi oggetto. Le funzioni di caricamento mesh D3DX riconoscono le istanze di modelli mesh, FrameTransformMatrix e frame come oggetti figlio durante il caricamento di un'istanza di frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876197"
---
# <a name="frame-direct3d-9-graphics"></a>Frame (grafica Direct3D 9)

Definisce un frame di coordinate o un "frame di riferimento". Il modello di frame è aperto e può contenere qualsiasi oggetto. Le funzioni di caricamento mesh D3DX riconoscono le istanze di modelli [**mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)e **frame** come oggetti figlio durante il caricamento di un'istanza di **frame** .

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

Il modello di frame riconosce i **nodi figlio e** i nodi [**mesh**](mesh.md) all'interno di un frame e può riconoscere i modelli definiti dall'utente tramite una funzione di callback.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



