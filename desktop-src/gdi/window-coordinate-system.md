---
description: Il sistema di coordinate per una finestra è basato sul sistema di coordinate del dispositivo di visualizzazione.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Sistema di coordinate finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755831"
---
# <a name="window-coordinate-system"></a>Sistema di coordinate finestra

Il sistema di coordinate per una finestra è basato sul sistema di coordinate del dispositivo di visualizzazione. L'unità di misura di base è l'unità del dispositivo, in genere il pixel. I punti sullo schermo sono descritti dalle coppie di coordinate x e y. Le coordinate x aumentano a destra; le coordinate y aumentano dall'alto verso il basso. L'origine (0,0) per il sistema dipende dal tipo di coordinate utilizzate.

Il sistema e le applicazioni specificano la posizione di una finestra sullo schermo in *coordinate dello schermo*. Per le coordinate dello schermo, l'origine è l'angolo superiore sinistro dello schermo. La posizione completa di una finestra è spesso descritta da una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) contenente le coordinate dello schermo di due punti che definiscono gli angoli superiore sinistro e inferiore destro della finestra.

Il sistema e le applicazioni specificano la posizione dei punti in una finestra usando le *coordinate client*. L'origine in questo caso è l'angolo superiore sinistro della finestra o dell'area client. Le coordinate client assicurano che un'applicazione possa usare valori di coordinate coerenti durante il disegno nella finestra, indipendentemente dalla posizione della finestra sullo schermo.

Le dimensioni dell'area client sono descritte anche da una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate client per l'area. In tutti i casi, la coordinata superiore sinistra del rettangolo viene inclusa nell'area della finestra o del client, mentre la coordinata inferiore destra viene esclusa. Le operazioni grafiche in una finestra o in un'area client sono escluse dai bordi destro e inferiore del rettangolo di inclusione.

Occasionalmente, le applicazioni potrebbero essere necessarie per eseguire il mapping delle coordinate in una finestra a quelle di un'altra finestra. Un'applicazione può mappare le coordinate usando la funzione [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) . Se una delle finestre è la finestra desktop, la funzione converte in modo efficace le coordinate dello schermo in coordinate client e viceversa; la finestra desktop è sempre specificata in coordinate dello schermo.

 

 
