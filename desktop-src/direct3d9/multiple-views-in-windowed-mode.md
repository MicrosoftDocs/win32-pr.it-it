---
description: Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo IDirect3DDevice9::CreateAdditionalSwapChain per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo.
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Più visualizzazioni in modalità finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2784a4f2bd855293e427aa9297d2e5725a74a3f5bce52b4b53cdf3d9081062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069021"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Più visualizzazioni in modalità finestra (Direct3D 9)

Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo.

In genere, l'applicazione crea una catena di scambio per ogni vista e associa ogni catena di scambio a una vista specifica. L'applicazione esegue il rendering delle immagini nei buffer back di ogni catena di scambio e quindi usa il metodo [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per presentarle singolarmente. Si noti che solo una catena di scambio alla volta può essere a schermo intero in ogni scheda.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 
