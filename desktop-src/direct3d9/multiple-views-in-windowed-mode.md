---
description: "Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo IDirect3DDevice9:: CreateAdditionalSwapChain per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo."
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Visualizzazioni multiple in modalità finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303920"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Visualizzazioni multiple in modalità finestra (Direct3D 9)

Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo.

In genere, l'applicazione crea una catena di scambio per ogni visualizzazione e associa ogni catena di scambio a una visualizzazione specifica. L'applicazione esegue il rendering delle immagini nei buffer indietro di ogni catena di scambio, quindi usa il metodo [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reinviato per presentarle singolarmente. Si noti che solo una catena di scambio alla volta può essere a schermo intero in ogni scheda.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 
