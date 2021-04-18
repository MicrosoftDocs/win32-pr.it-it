---
description: Molte applicazioni C++ cancellano il buffer di profondità prima di eseguire il rendering di ogni nuovo frame.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Cancellazione dei buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304798"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Cancellazione dei buffer di profondità (Direct3D 9)

Molte applicazioni C++ cancellano il buffer di profondità prima di eseguire il rendering di ogni nuovo frame. È possibile cancellare in modo esplicito il buffer di profondità tramite Direct3D chiamando [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) e specificando D3DCLEAR \_ ZBUFFER per il parametro flags. Il metodo **IDirect3DDevice9:: Clear** consente di specificare un valore di profondità arbitrario nel parametro Z.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
