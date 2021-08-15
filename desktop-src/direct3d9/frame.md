---
description: Definisce un frame di coordinate, o &\# 0034;frame di reference.&\# 0034; Il modello Frame è aperto e può contenere qualsiasi oggetto. Le funzioni di caricamento mesh D3DX riconoscono le istanze del modello Mesh, FrameTransformMatrix e Frame come oggetti figlio durante il caricamento di un'istanza Frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523034"
---
# <a name="frame-direct3d-9-graphics"></a>Frame (grafica Direct3D 9)

Definisce un frame di coordinate, o "frame di riferimento". Il modello Frame è aperto e può contenere qualsiasi oggetto. Le funzioni di caricamento mesh D3DX riconoscono le istanze del modello [**Mesh,**](mesh.md) [**FrameTransformMatrix**](frametransformmatrix.md)e **Frame** come oggetti figlio durante il caricamento di un'istanza **Frame.**

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

Il modello di frame riconosce i nodi **figlio Frame** e [**Mesh**](mesh.md) all'interno di un frame e può riconoscere i modelli definiti dall'utente tramite una funzione di callback.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



