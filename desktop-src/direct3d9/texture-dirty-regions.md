---
description: Le applicazioni possono ottimizzare il subset di una trama che viene copiato specificando &\# 0034; dirty&\# 0034; aree nelle trame.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Aree dirty texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304108"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Aree dirty texture (Direct3D 9)

Le applicazioni possono ottimizzare il subset di una trama che viene copiato specificando aree "Dirty" nelle trame. Solo le aree contrassegnate come dirty vengono copiate da una chiamata a [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture). Tuttavia, le aree dirty possono essere espanse per ottimizzare l'allineamento. Quando viene creata una trama, l'intera trama viene considerata Dirty. Solo le operazioni seguenti influiscono sullo stato dirty di una trama:

-   Aggiunta di un'area dirty a una trama.
-   Blocco di un buffer nella trama. Questa operazione aggiunge l'area bloccata come area dirty. L'applicazione può disattivare questo aggiornamento automatico dell'area dirty se dispone di una conoscenza più approfondita delle aree dirty effettive.
-   Se si usa un livello di superficie della trama come destinazione in [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , l'intera trama viene contrassegnata come dirty.
-   L'uso della trama come origine in [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) Cancella tutte le aree dirty sulla trama di origine.
-   Uso di [**IDirect3DSurface9:: GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) per restituire un contesto di dispositivo.
-   La chiamata di [**IDirect3DBaseTexture9:: GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) contrassegna l'intera trama come dirty.
-   La chiamata di [**IDirect3DBaseTexture9:: SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) contrassegna l'intera trama come dirty.

Le aree dirty vengono impostate sul primo livello di una trama mipmap e [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) può espandere l'area dirty nella catena MIP per ridurre al minimo il numero di byte copiati per ogni sottolivello. Si noti che le coordinate dell'area dirty del sottolivello vengono arrotondate verso l'esterno, ovvero le parti frazionarie vengono arrotondate al bordo più vicino della trama.

Poiché ogni tipo di trama presenta tipi diversi di aree dirty, esistono metodi su ogni tipo di trama. le trame 2D usano rettangoli Dirty e le trame del volume usano le caselle.

-   [**IDirect3DCubeTexture9:: AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9:: AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Il passaggio di un **valore null** per i parametri PDirtyRect o pDirtyBox per i metodi precedenti espande l'area dirty per coprire l'intera trama.

Ogni metodo Lock può eseguire D3DLOCK \_ senza \_ \_ aggiornamento Dirty, che impedisce qualsiasi modifica allo stato dirty della trama. Per altre informazioni, vedere [blocco di risorse (Direct3D 9)](locking-resources.md).

Quando sono disponibili ulteriori informazioni sul vero set di aree modificate durante un'operazione di blocco, le applicazioni devono utilizzare D3DLOCK \_ senza \_ aggiornamenti Dirty \_ . Si noti che un blocco o una copia in un solo sottolivello di trama, ovvero senza blocco o copia al livello superiore, non aggiorna le aree dirty per tale trama. Le applicazioni assumono la stessa responsabilità di aggiornare le aree dirty quando bloccano i livelli inferiori senza bloccare il livello superiore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
