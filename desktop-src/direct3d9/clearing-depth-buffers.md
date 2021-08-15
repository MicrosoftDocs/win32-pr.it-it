---
description: Molte applicazioni C++ cancellano il buffer di profondità prima di eseguire il rendering di ogni nuovo frame.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Cancellazione dei buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989311"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Cancellazione dei buffer di profondità (Direct3D 9)

Molte applicazioni C++ cancellano il buffer di profondità prima di eseguire il rendering di ogni nuovo frame. È possibile cancellare in modo esplicito il buffer di profondità tramite Direct3D chiamando [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) e specificando D3DCLEAR ZBUFFER per \_ il parametro Flags. Il **metodo IDirect3DDevice9::Clear** consente di specificare un valore di profondità arbitrario nel parametro Z.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
