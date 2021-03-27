---
description: Un contesto di dispositivo finestra consente a un'applicazione di creare qualsiasi punto in una finestra, inclusa l'area non client.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Visualizzazione dei contesti di dispositivo della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75abed6177771d9beff56ad5e7dec1f8e0a704c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979367"
---
# <a name="window-display-device-contexts"></a>Visualizzazione dei contesti di dispositivo della finestra

Un *contesto di dispositivo finestra* consente a un'applicazione di creare qualsiasi punto in una finestra, inclusa l'area non client. I contesti di dispositivo Windows vengono in genere usati da applicazioni che elaborano i messaggi [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per Windows con aree non client personalizzate. L'uso di un contesto di dispositivo Windows non è consigliato per altri scopi.

Un'applicazione può recuperare un contesto di dispositivo della finestra usando la funzione [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con l' \_ opzione della finestra DCX specificata. La funzione recupera un contesto di dispositivo della finestra dalla cache del contesto del dispositivo di visualizzazione. Una finestra che usa un contesto di dispositivo della finestra deve rilasciarla dopo il disegno usando la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) il prima possibile. I contesti di dispositivo Windows sono sempre dalla cache; gli \_ stili della classe CS OWNDC e cs \_ CLASSDC non influiscono sul contesto di dispositivo.

Quando un'applicazione recupera un contesto di dispositivo della finestra, il sistema imposta l'origine del dispositivo sull'angolo superiore sinistro della finestra anziché sull'angolo superiore sinistro dell'area client. Imposta anche l'area di visualizzazione per includere l'intera finestra, non solo l'area client. Il sistema imposta i valori di attributo correnti di un contesto di dispositivo della finestra sugli stessi valori predefiniti di un contesto di dispositivo comune. Un'applicazione può modificare i valori di attributo, ma il sistema non mantiene alcuna modifica quando viene rilasciato il contesto di dispositivo.

 

 
