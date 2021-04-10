---
description: Le risorse sono le trame e i buffer usati per eseguire il rendering di una scena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Risorse Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124497"
---
# <a name="direct3d-resources-direct3d-9"></a>Risorse Direct3D (Direct3D 9)

Le risorse sono le trame e i buffer usati per eseguire il rendering di una scena. Le applicazioni devono creare, caricare, copiare e usare le risorse. Questa sezione fornisce una breve introduzione alle risorse e ai passaggi e ai metodi usati dalle applicazioni per l'uso delle risorse.

Tutte le risorse, incluse le risorse Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) e [**IDirect3DVertexBuffer9**](/windows/desktop/api), ereditano dall'interfaccia [**IDirect3DResource9**](/windows/desktop/api) . Le risorse di trama, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9**](/windows/desktop/api), ereditano anche dall'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .

-   [Proprietà delle risorse (Direct3D 9)](resource-properties.md)
-   [Manipolazione di risorse (Direct3D 9)](manipulating-resources.md)
-   [Blocco di risorse (Direct3D 9)](locking-resources.md)
-   [Relazioni tra risorse (Direct3D 9)](resource-relationships.md)
-   [Gestione delle risorse (Direct3D 9)](managing-resources.md)
-   [Risorse gestite dall'applicazione e strategie di allocazione (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Buffer di indice (Direct3D 9)](index-buffers.md)
-   [Buffer vertex (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
