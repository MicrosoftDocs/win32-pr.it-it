---
title: Uso degli stili della finestra per modificare la finestra MCIWnd
description: Uso degli stili della finestra per modificare la finestra MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299672"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Uso degli stili della finestra per modificare la finestra MCIWnd

Come con qualsiasi finestra, è possibile modificare l'aspetto e il comportamento di una finestra MCIWnd scegliendo tra gli stili standard della finestra specificati con la funzione [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Inoltre, è possibile scegliere tra diversi altri stili di finestra specifici per le finestre di MCIWnd. Con questi stili, l'applicazione può modificare le finestre MCIWnd nei modi seguenti:

-   Modificare le dimensioni della finestra.
-   Nascondere o visualizzare i controlli.
-   Invia messaggi di notifica.
-   Visualizzare le informazioni nella barra del titolo.

Per impostare gli stili della finestra, è possibile specificarli nella funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) oppure usare la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) per modificare lo stile di una finestra di MCIWnd esistente. È anche possibile eseguire una query su una finestra MCIWnd per gli stili correnti usando la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .

Per un elenco degli stili della finestra specifici di MCIWnd, vedere [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 