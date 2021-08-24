---
description: Panoramica della denominazione appropriata di una finestra e dell'impostazione della didascalia della finestra per il Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Denominazione appropriata di una finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f2109568306e8817c518eecd8761ab00a2b1ecb8c54d4388b78e3eb456278d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883401"
---
# <a name="naming-a-window-appropriately"></a>Denominazione appropriata di una finestra

Assegnare a ogni finestra una didascalia descrittiva, anche se la finestra o la relativa didascalia è invisibile. Ciò consente alla funzionalità di riconoscimento vocale di identificare la finestra e la gerarchia della finestra. Questa raccomandazione si applica a tutte le finestre: finestre di primo livello con frame visibili. finestre figlio, ad esempio tavolozze mobili; controlli personalizzati; barre degli strumenti; riquadri e all'interno di una finestra, se implementati come finestre figlio.

Esistono tre modi per impostare la didascalia della finestra:

-   Impostare la stringa nello script della risorsa quando si chiama [**CreateWindow o**](/windows/desktop/api/winuser/nf-winuser-createwindowa) le funzioni correlate.
-   Chiamare la [**funzione SetWindowText.**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)
-   Definire il nome dei controlli nelle finestre di dialogo usando le tecniche descritte in [Denominazione dei controlli nelle finestre di dialogo](naming-controls-in-dialog-boxes.md). Questo è l'unico metodo per l'etichettatura di un controllo di modifica, perché l'impostazione dell'etichetta intrinseca dei controlli modifica il contenuto dei controlli.

È possibile eseguire una query sulla didascalia usando Microsoft Active Accessibility o il messaggio WM \_ GETTEXT.

Per altre informazioni sull'esecuzione di query sulla didascalia Active Accessibility, vedere la [sezione Accessibilità.](/windows/desktop/accessibility)

 

 
