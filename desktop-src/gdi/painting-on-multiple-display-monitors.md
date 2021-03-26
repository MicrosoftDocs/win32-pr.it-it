---
description: Il sistema gestisce automaticamente il disegno in un contesto di dispositivo (DC) che si estende su più di un monitor, anche quando i monitoraggi hanno profondità dei colori differenti.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Disegno su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754343"
---
# <a name="painting-on-multiple-display-monitors"></a>Disegno su più monitor di visualizzazione

Il sistema gestisce automaticamente il disegno in un contesto di dispositivo (DC) che si estende su più di un monitor, anche quando i monitoraggi hanno profondità dei colori differenti. In genere, questo produce risultati ottimali, ma potrebbe non essere ottimale. Ad esempio, una finestra su due monitoraggi di profondità dei colori notevolmente diverse potrebbe avere una resa dei colori scadente. Inoltre, i monitoraggi con la stessa profondità di colore possono avere un esempio di colore systemper diverso, i colori possono essere codificati con numeri di bit diversi o essere posizionati in posizioni diverse nel valore di colore di un pixel.

Per ottenere risultati ottimali per ognuno dei monitoraggi in un controller di dominio che si estende su più di una visualizzazione, chiamare [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) per enumerare i monitoraggi che intersecano il controller di dominio e disegnare l'area di intersezione in ognuno di essi separatamente in base agli attributi di visualizzazione per il monitoraggio. Vedere l'esempio in [disegnare in un controller di dominio che si estende su più schermi](painting-on-a-dc-that-spans-multiple-displays.md).

Se si esegue tutto il disegno nel codice di **disegno \_ WM** e se il codice **\_ di disegno WM** gestisce tutte le varie modalità video, sarà possibile inserire il codice di disegno **\_ WM** nel **MonitorEnumProc** di [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) con solo alcune modifiche.

 

 



