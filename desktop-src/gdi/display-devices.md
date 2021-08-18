---
description: Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Dispositivi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd71b943d294bf89e932f965b023ecbce7f4e594044fe96b70bb84d41a27f777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038119"
---
# <a name="display-devices"></a>Dispositivi di visualizzazione

Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno. Un contesto di dispositivo di visualizzazione definisce un set di oggetti grafici e i relativi attributi associati e le modalità grafiche che influiscono sull'output. Il sistema prepara ogni contesto di dispositivo di visualizzazione per l'output in una finestra, impostando gli oggetti, i colori e le modalità di disegno per la finestra anziché per il dispositivo di visualizzazione. Quando l'applicazione fornisce il contesto di dispositivo di visualizzazione tramite chiamate alle funzioni GDI, GDI usa le informazioni nel contesto per generare l'output nella finestra specificata senza intrusire su altre finestre o altre parti dello schermo.

Il sistema fornisce cinque tipi di contesti di dispositivo di visualizzazione.



| Type                                           | Significato                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comune](common-display-device-contexts.md)   | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [class](class-display-device-contexts.md)     | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Consente di disegnare in un punto qualsiasi della finestra. Anche se il contesto di dispositivo padre consente anche il disegno nella finestra padre, non deve essere usato in questo modo. |
| [Privato](private-display-device-contexts.md) | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [Finestra](window-display-device-contexts.md)   | Consente di disegnare in un punto qualsiasi della finestra.                                                                                                                          |



 

Il sistema fornisce un contesto di dispositivo comune, classe, padre o privato a una finestra in base al tipo di contesto di dispositivo di visualizzazione specificato nello stile della classe della finestra. Il sistema fornisce un contesto di dispositivo della finestra solo quando l'applicazione ne richiede uno in modo esplicito, ad esempio chiamando la [**funzione GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx.**](/windows/desktop/api/Winuser/nf-winuser-getdcex) In tutti i casi, un'applicazione può usare la [**funzione WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) per determinare quale finestra rappresenta attualmente un controller di dominio di visualizzazione.

In questa sezione vengono fornite informazioni sugli argomenti seguenti.

-   [Visualizzare la cache del contesto di dispositivo](display-device-context-cache.md)
-   [Visualizzare i valori predefiniti del contesto di dispositivo](display-device-context-defaults.md)
-   [Contesti di dispositivo di visualizzazione comuni](common-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione privati](private-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione padre](parent-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione delle classi](class-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione della finestra](window-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione padre](parent-display-device-contexts.md)

 

 



