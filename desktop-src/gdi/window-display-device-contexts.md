---
description: Un contesto di dispositivo della finestra consente a un'applicazione di disegnare in qualsiasi punto di una finestra, inclusa l'area non client.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Contesti di dispositivo di visualizzazione della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfed34646323114ffcfb7753331b1b5c305a7a0c01a475795a7918f6e5a2dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965091"
---
# <a name="window-display-device-contexts"></a>Contesti di dispositivo di visualizzazione della finestra

Un *contesto di dispositivo della* finestra consente a un'applicazione di disegnare in qualsiasi punto di una finestra, inclusa l'area non client. I contesti di dispositivo della finestra vengono in genere usati dalle applicazioni che elaborano i messaggi [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per le finestre con aree non client personalizzate. L'uso di un contesto di dispositivo della finestra non è consigliato per altri scopi.

Un'applicazione può recuperare un contesto di dispositivo della finestra usando la [**funzione GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con l'opzione DCX \_ WINDOW specificata. La funzione recupera un contesto di dispositivo della finestra dalla cache del contesto di dispositivo di visualizzazione. Una finestra che usa un contesto di dispositivo della finestra deve rilasciarla dopo il disegno usando la [**funzione ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) appena possibile. I contesti di dispositivo della finestra vengono sempre dalla cache. Gli stili delle classi CS OWNDC e \_ CS \_ CLASSDC non influiscono sul contesto di dispositivo.

Quando un'applicazione recupera un contesto di dispositivo della finestra, il sistema imposta l'origine del dispositivo sull'angolo superiore sinistro della finestra anziché sull'angolo superiore sinistro dell'area client. Imposta anche l'area di ritaglio in modo da includere l'intera finestra, non solo l'area client. Il sistema imposta i valori dell'attributo corrente di un contesto di dispositivo della finestra sullo stesso valore predefinito di un contesto di dispositivo comune. Un'applicazione può modificare i valori degli attributi, ma il sistema non mantiene alcuna modifica quando viene rilasciato il contesto di dispositivo.

 

 
