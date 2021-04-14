---
description: I metodi del cursore del mouse consentono all'applicazione di specificare un cursore di colore fornendo una superficie che contiene un'immagine.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Utilizzo dei cursori del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482413"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Utilizzo dei cursori del mouse (Direct3D 9)

I metodi del cursore del mouse consentono all'applicazione di specificare un cursore di colore fornendo una superficie che contiene un'immagine. Il sistema garantisce che questo cursore venga aggiornato a metà della frequenza di visualizzazione o superiore se la frequenza dei fotogrammi dell'applicazione è lenta. Tuttavia, il cursore non verrà mai aggiornato più di frequente rispetto alla frequenza di aggiornamento dello schermo.

La posizione del cursore del mouse è associata al cursore di sistema, ridimensionata in modo appropriato per la risoluzione spaziale della modalità di visualizzazione corrente, ma può essere spostata in modo esplicito dall'applicazione. Questo comportamento è analogo al comportamento del cursore del mouse di sistema supportato dall'API Win32. Per ulteriori informazioni sull'utilizzo di un cursore del mouse nell'applicazione Direct3D, vedere gli argomenti di riferimento seguenti.

-   [**IDirect3DDevice9:: ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9:: SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9:: SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D garantisce che il mouse sia supportato dalle implementazioni hardware o dal tempo di esecuzione Direct3D che esegue operazioni blitting con accelerazione hardware durante la chiamata di [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
