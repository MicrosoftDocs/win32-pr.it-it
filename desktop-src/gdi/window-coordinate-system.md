---
description: Il sistema di coordinate per una finestra è basato sul sistema di coordinate del dispositivo di visualizzazione.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Sistema di coordinate della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c5492aaa02e1b2b2ace7e0cb02a65caa1faad320eca11414707145066308e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717871"
---
# <a name="window-coordinate-system"></a>Sistema di coordinate della finestra

Il sistema di coordinate per una finestra è basato sul sistema di coordinate del dispositivo di visualizzazione. L'unità di misura di base è l'unità del dispositivo (in genere, il pixel). I punti sullo schermo sono descritti da coppie di coordinate x e y. Le coordinate x aumentano a destra. Le coordinate y aumentano dall'alto verso il basso. L'origine (0,0) per il sistema dipende dal tipo di coordinate in uso.

Il sistema e le applicazioni specificano la posizione di una finestra sullo schermo nelle *coordinate dello schermo.* Per le coordinate dello schermo, l'origine è l'angolo superiore sinistro dello schermo. La posizione completa di una finestra è spesso descritta da una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) contenente le coordinate dello schermo di due punti che definiscono gli angoli superiore sinistro e inferiore destro della finestra.

Il sistema e le applicazioni specificano la posizione dei punti in una finestra usando le *coordinate client*. L'origine in questo caso è l'angolo superiore sinistro della finestra o dell'area client. Le coordinate client garantiscono che un'applicazione possa usare valori di coordinate coerenti durante il disegno nella finestra, indipendentemente dalla posizione della finestra sullo schermo.

Le dimensioni dell'area client sono descritte anche da una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate client per l'area. In tutti i casi, la coordinata superiore sinistra del rettangolo è inclusa nella finestra o nell'area client, mentre la coordinata inferiore destra è esclusa. Le operazioni grafiche in una finestra o in un'area client vengono escluse dai bordi destro e inferiore del rettangolo di inclusione.

In alcuni casi, potrebbe essere necessario eseguire il mapping delle coordinate in una finestra a quelle di un'altra finestra. Un'applicazione può eseguire il mapping delle coordinate usando la [**funzione MapWindowPoints.**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) Se una delle finestre è la finestra desktop, la funzione converte in modo efficace le coordinate dello schermo in coordinate client e viceversa. la finestra del desktop è sempre specificata nelle coordinate dello schermo.

 

 
