---
description: I metodi del cursore del mouse consentono all'applicazione di specificare un cursore colore fornendo una superficie che contiene un'immagine.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Utilizzo dei cursori del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518919"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Utilizzo dei cursori del mouse (Direct3D 9)

I metodi del cursore del mouse consentono all'applicazione di specificare un cursore colore fornendo una superficie che contiene un'immagine. Il sistema garantisce che il cursore verrà aggiornato a metà della frequenza di visualizzazione o superiore se la frequenza dei fotogrammi dell'applicazione è lenta. Tuttavia, il cursore non verrà mai aggiornato con maggiore frequenza rispetto alla frequenza di aggiornamento della visualizzazione.

La posizione del cursore del mouse è associata al cursore di sistema, ridimensionata in modo appropriato per la risoluzione spaziale della modalità di visualizzazione corrente, ma può essere spostata in modo esplicito dall'applicazione. Questo comportamento è analogo al comportamento dell'API Win32: cursore del mouse di sistema supportato. Per altre informazioni su come usare un cursore del mouse nell'applicazione Direct3D, vedere gli argomenti di riferimento seguenti.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D garantisce che il mouse sia supportato dalle implementazioni hardware o dal tempo di esecuzione Direct3D che esegue operazioni di btting con accelerazione hardware quando si chiama [**IDirect3DDevice9::P resent.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 
