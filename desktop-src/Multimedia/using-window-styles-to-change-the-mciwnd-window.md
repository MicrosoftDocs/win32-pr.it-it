---
title: Uso degli stili della finestra per modificare la finestra MCIWnd
description: Uso degli stili della finestra per modificare la finestra MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Funzione MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90212b43d6d51c82eb9b6e1a26bb06c7215c2568594e04980294b0d87bd53e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135609"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Uso degli stili della finestra per modificare la finestra MCIWnd

Come per qualsiasi finestra, è possibile modificare l'aspetto e il comportamento di una finestra MCIWnd scegliendo tra gli stili di finestra standard specificati con la [funzione CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) È anche possibile scegliere tra diversi altri stili di finestra specifici delle finestre MCIWnd. Con questi stili, l'applicazione può modificare queste finestre MCIWnd nei modi seguenti:

-   Modificare le dimensioni della finestra.
-   Nascondere o visualizzare i controlli.
-   Invia messaggi di notifica.
-   Visualizzare le informazioni nella barra del titolo.

È possibile impostare gli stili della finestra specificandoli nella funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) oppure è possibile usare la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) per modificare lo stile di una finestra MCIWnd esistente. È anche possibile eseguire una query su una finestra MCIWnd per i relativi stili correnti usando la macro [**MCIWndGetStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)

Per un elenco degli stili di finestra specifici di MCIWnd, vedere [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 