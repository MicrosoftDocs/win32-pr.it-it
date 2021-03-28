---
description: Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Dispositivi di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978658"
---
# <a name="display-devices"></a>Dispositivi di visualizzazione

Prima di disegnare, il sistema deve preparare il dispositivo di visualizzazione per le operazioni di disegno. Un contesto di dispositivo di visualizzazione definisce un set di oggetti grafici e i relativi attributi associati, nonché le modalità grafiche che interessano l'output. Il sistema prepara ogni contesto di dispositivo di visualizzazione per l'output in una finestra, impostando gli oggetti, i colori e le modalità di disegno per la finestra anziché il dispositivo di visualizzazione. Quando l'applicazione fornisce il contesto del dispositivo di visualizzazione tramite le chiamate alle funzioni GDI, GDI USA le informazioni nel contesto per generare l'output nella finestra specificata senza intrusioni in altre finestre o altre parti dello schermo.

Il sistema offre cinque tipi di contesti di dispositivo di visualizzazione.



| Type                                           | Significato                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [comune](common-display-device-contexts.md)   | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [class](class-display-device-contexts.md)     | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Consente di disegnare in un punto qualsiasi della finestra. Sebbene il contesto di dispositivo padre consenta anche il disegno nella finestra padre, non è destinato a essere utilizzato in questo modo. |
| [privata](private-display-device-contexts.md) | Consente il disegno nell'area client di una finestra specificata.                                                                                                        |
| [finestra](window-display-device-contexts.md)   | Consente di disegnare in un punto qualsiasi della finestra.                                                                                                                          |



 

Il sistema fornisce un contesto di dispositivo comune, di classe, padre o privato a una finestra in base al tipo di contesto del dispositivo di visualizzazione specificato nello stile della classe di tale finestra. Il sistema fornisce un contesto di dispositivo finestra solo quando l'applicazione ne richiede esplicitamente uno, ad esempio chiamando la funzione [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) . In tutti i casi, un'applicazione può usare la funzione [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) per determinare la finestra attualmente rappresentata da un controller di dominio di visualizzazione.

In questa sezione vengono fornite informazioni sui seguenti argomenti.

-   [Visualizza la cache del contesto del dispositivo](display-device-context-cache.md)
-   [Visualizzare le impostazioni predefinite del contesto di dispositivo](display-device-context-defaults.md)
-   [Contesti di dispositivo di visualizzazione comuni](common-display-device-contexts.md)
-   [Contesti di dispositivo di visualizzazione privati](private-display-device-contexts.md)
-   [Contesti dispositivo di visualizzazione padre](parent-display-device-contexts.md)
-   [Classe Visualizza contesti di dispositivo](class-display-device-contexts.md)
-   [Visualizzazione dei contesti di dispositivo della finestra](window-display-device-contexts.md)
-   [Contesti dispositivo di visualizzazione padre](parent-display-device-contexts.md)

 

 



