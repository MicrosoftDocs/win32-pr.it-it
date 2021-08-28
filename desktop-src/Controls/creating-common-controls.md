---
title: Creazione di controlli comuni
description: Questo argomento descrive come creare una finestra che appartiene a una classe di finestra definita nella libreria di controlli comune, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ddc06def47cef1a34849bbe31bc3871d4c098890bd3ef53830ae6fe7076520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916341"
---
# <a name="creating-common-controls"></a>Creazione di controlli comuni

Questo argomento descrive come creare una finestra che appartiene a una classe di finestra definita nella libreria di controlli comune, Comctl32.dll.


I controlli più comuni appartengono a una classe finestra definita nella DLL dei controlli comuni. La classe window e la routine della finestra corrispondente definiscono le proprietà, l'aspetto e il comportamento del controllo. Per assicurarsi che la DLL del controllo comune sia caricata, includere la [**funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) nell'applicazione. È possibile creare un controllo comune specificando il nome della classe finestra quando si chiama la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o specificando il nome della classe appropriato in un modello di finestra di dialogo.


Ogni tipo di controllo comune ha un set di stili di controllo che è possibile usare per variare l'aspetto e il comportamento del controllo. La libreria di controlli comune include anche un set di stili di controllo che si applicano a due o più tipi di controlli comuni. Gli stili dei controlli comuni sono descritti nella [sezione Stili.](common-control-styles.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 