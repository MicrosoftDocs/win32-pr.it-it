---
description: Per impostazione predefinita, il sistema Direct3D può scrivere nel buffer di profondità. La maggior parte delle applicazioni lascia la scrittura nel buffer di profondità abilitato, ma è possibile ottenere alcuni effetti speciali non consentendo al sistema Direct3D di scrivere nel buffer di profondità.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Modifica dell'accesso in scrittura al buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304799"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Modifica dell'accesso in scrittura al buffer di profondità (Direct3D 9)

Per impostazione predefinita, il sistema Direct3D può scrivere nel buffer di profondità. La maggior parte delle applicazioni lascia la scrittura nel buffer di profondità abilitato, ma è possibile ottenere alcuni effetti speciali non consentendo al sistema Direct3D di scrivere nel buffer di profondità.

È possibile disabilitare le Scritture del buffer di profondità in C++ chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con il parametro state impostato su D3DRS \_ ZWRITEENABLE e il parametro value impostato su 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
