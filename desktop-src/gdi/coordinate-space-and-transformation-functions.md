---
description: Le funzioni seguenti vengono utilizzate con gli spazi delle coordinate e le trasformazioni.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Spazio delle coordinate e funzioni di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e561f5cc9784439f5bef4f696e98d5919cb052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226703"
---
# <a name="coordinate-space-and-transformation-functions"></a>Spazio delle coordinate e funzioni di trasformazione

Le funzioni seguenti vengono utilizzate con gli spazi delle coordinate e le trasformazioni.



| Funzione                                                                       | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Converte le coordinate dell'area client di un punto specificato in coordinate dello schermo.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Concatena due trasformazioni dello spazio globale in pagine.                                                                      |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Converte le coordinate del dispositivo in coordinate logiche.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Recupera la posizione corrente nelle coordinate logiche.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Ottiene le preferenze di orientamento della visualizzazione.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Recupera la modalità grafica corrente per il contesto di dispositivo specificato.                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Recupera la modalità di mapping corrente.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Recupera l'extent x e l'extent y del viewport corrente per il contesto di dispositivo specificato.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Recupera le coordinate x e y dell'origine del viewport per il contesto di dispositivo specificato.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Recupera l'extent x e l'extent y della finestra per il contesto di dispositivo specificato.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Recupera le coordinate x e y dell'origine della finestra per il contesto di dispositivo specificato.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Recupera lo spazio globale corrente nella trasformazione dello spazio pagina.                                                                  |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Converte le coordinate logiche in coordinate del dispositivo.                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Converte (esegue il mapping) un set di punti da uno spazio delle coordinate rispetto a una finestra a uno spazio delle coordinate relativo a un'altra finestra. |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Modifica la trasformazione globale per un contesto di dispositivo utilizzando la modalità specificata.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Modifica l'origine del viewport per un contesto di dispositivo utilizzando gli offset orizzontali e verticali specificati.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Modifica l'origine della finestra per un contesto di dispositivo utilizzando gli offset orizzontali e verticali specificati.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Modifica il viewport per un contesto di dispositivo utilizzando i rapporti formati dai multiplicands e dai divisori specificati.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Modifica la finestra per un contesto di dispositivo utilizzando i rapporti formati dai multiplicands e dai divisori specificati.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Converte le coordinate dello schermo di un punto specificato sullo schermo in coordinate client.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Imposta le preferenze di orientamento della visualizzazione.                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Imposta la modalità grafica per il contesto di dispositivo specificato.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Imposta la modalità di mapping del contesto di dispositivo specificato.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Imposta gli extent orizzontali e verticali del viewport per un contesto di dispositivo utilizzando i valori specificati.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Specifica il punto del dispositivo mappato all'origine della finestra (0,0).                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Imposta gli extent orizzontali e verticali della finestra per un contesto di dispositivo utilizzando i valori specificati.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Specifica quale punto della finestra viene mappato all'origine del viewport (0, 0).                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Imposta una trasformazione lineare bidimensionale tra spazio globale e spazio della pagina per il contesto di dispositivo specificato.                |



 

 

 
