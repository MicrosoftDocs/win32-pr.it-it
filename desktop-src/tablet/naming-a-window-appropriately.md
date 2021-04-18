---
description: Cenni preliminari sulla denominazione di una finestra in modo appropriato e sull'impostazione della didascalia della finestra per Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Assegnazione di un nome a una finestra in modo appropriato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315562"
---
# <a name="naming-a-window-appropriately"></a>Assegnazione di un nome a una finestra in modo appropriato

Assegnare a ogni finestra una didascalia intuitiva, anche se la finestra o la relativa didascalia è invisibile. Questo consente la funzionalità di riconoscimento vocale per identificare la finestra e la gerarchia della finestra. Questa raccomandazione si applica a tutte le finestre: finestre di primo livello con frame visibili; finestre figlio, ad esempio tavolozze mobili; controlli personalizzati; barre degli strumenti e riquadri in una finestra, quando vengono implementati come finestre figlio.

È possibile impostare la didascalia della finestra in tre modi:

-   Impostare la stringa nello script della risorsa durante la chiamata di [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o delle funzioni correlate.
-   Chiamare la funzione [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .
-   Definire il nome dei controlli nelle finestre di dialogo utilizzando le tecniche descritte in [denominare i controlli nelle finestre di dialogo](naming-controls-in-dialog-boxes.md). Questo è l'unico metodo per etichettare un controllo di modifica, perché l'impostazione dell'etichetta intrinseca Controls modifica il contenuto dei controlli.

È possibile eseguire una query sulla didascalia usando Microsoft Active Accessibility o il \_ messaggio WM gettext.

Per ulteriori informazioni sull'esecuzione di query sulla didascalia utilizzando Active Accessibility, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) .

 

 
