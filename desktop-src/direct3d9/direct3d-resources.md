---
description: Le risorse sono trame e buffer usati per eseguire il rendering di una scena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Risorse Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acc40cc929f5cedbefaa0b652c67ea59e35212e4da81c4278e3a57f48ea7662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523780"
---
# <a name="direct3d-resources-direct3d-9"></a>Risorse Direct3D (Direct3D 9)

Le risorse sono trame e buffer usati per eseguire il rendering di una scena. Le applicazioni devono creare, caricare, copiare e usare le risorse. Questa sezione offre una breve introduzione alle risorse e ai passaggi e ai metodi usati dalle applicazioni quando si lavora con le risorse.

Tutte le risorse, incluse le risorse geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) e [**IDirect3DVertexBuffer9,**](/windows/desktop/api)ereditano dall'interfaccia [**IDirect3DResource9.**](/windows/desktop/api) Anche le risorse di [**trama, IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9**](/windows/desktop/api), ereditano dall'interfaccia [**IDirect3DBaseTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)

-   [Proprietà risorsa (Direct3D 9)](resource-properties.md)
-   [Manipolazione delle risorse (Direct3D 9)](manipulating-resources.md)
-   [Blocco delle risorse (Direct3D 9)](locking-resources.md)
-   [Relazioni tra risorse (Direct3D 9)](resource-relationships.md)
-   [Gestione delle risorse (Direct3D 9)](managing-resources.md)
-   [Risorse gestite dall'applicazione e strategie di allocazione (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Buffer di indice (Direct3D 9)](index-buffers.md)
-   [Vertex Buffers (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
