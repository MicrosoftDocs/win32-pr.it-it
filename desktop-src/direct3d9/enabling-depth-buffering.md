---
description: 'Dopo aver creato un buffer di profondità, come descritto in creazione di un buffer di profondità (Direct3D 9), è possibile abilitare la memorizzazione nel buffer di profondità chiamando il metodo IDirect3DDevice9:: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Abilitazione del buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341426"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Abilitazione del buffer di profondità (Direct3D 9)

Dopo aver creato un buffer di profondità, come descritto in [creazione di un buffer di profondità (Direct3D 9)](creating-a-depth-buffer.md), è possibile abilitare la memorizzazione nel buffer di profondità chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) . Impostare lo \_ stato di rendering ZENABLE di D3DRS per abilitare il buffering di profondità. Usare il \_ membro D3DZB true del tipo enumerato [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (o **true**) per abilitare il buffering z, D3DZB \_ USEW per abilitare w-buffering oppure D3DZB \_ false (o **false**) per disabilitare il buffering di profondità.

> [!Note]  
> Per usare il buffering w, l'applicazione deve impostare una matrice di proiezione conforme anche se non usa la pipeline di trasformazione Direct3D. Per informazioni su come fornire una matrice di proiezione appropriata, vedere [una matrice di proiezione W-friendly](projection-transform.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
