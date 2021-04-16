---
description: Oltre alla catena di scambio di proprietà e manipolata tramite l'interfaccia IDirect3DDevice9, un'applicazione può creare altre catene di scambio per presentare più visualizzazioni dallo stesso dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Presentazione di più visualizzazioni in modalità finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522769"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Presentazione di più visualizzazioni in modalità finestra (Direct3D 9)

Oltre alla catena di scambio di proprietà e manipolata tramite l'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) , un'applicazione può creare altre catene di scambio per presentare più visualizzazioni dallo stesso dispositivo. L'applicazione crea in genere una catena di scambio per ogni visualizzazione usando il metodo [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e associa ogni catena di scambio a una determinata finestra. L'applicazione esegue il rendering delle immagini nei buffer indietro di ogni catena di scambio e quindi le presenta singolarmente.

Solo una catena di scambio alla volta può essere a schermo intero in ogni scheda.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
