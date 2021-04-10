---
title: Creazione di controlli comuni
description: In questo argomento viene descritto come creare una finestra che appartiene a una classe della finestra definita nella libreria di controlli comuni Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963567"
---
# <a name="creating-common-controls"></a>Creazione di controlli comuni

In questo argomento viene descritto come creare una finestra che appartiene a una classe della finestra definita nella libreria di controlli comuni Comctl32.dll.


La maggior parte dei controlli comuni appartiene a una classe della finestra definita nella DLL del controllo comune. La classe della finestra e la corrispondente routine della finestra definiscono le proprietà, l'aspetto e il comportamento del controllo. Per assicurarsi che la DLL del controllo comune sia caricata, includere la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) nell'applicazione. È possibile creare un controllo comune specificando il nome della classe della finestra quando si chiama la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o specificando il nome della classe appropriato in un modello di finestra di dialogo.


Ogni tipo di controllo comune ha un set di stili di controllo che è possibile usare per variare l'aspetto e il comportamento del controllo. La libreria di controlli comuni include anche un set di stili di controllo che si applicano a due o più tipi di controlli comuni. Gli stili di controllo comuni sono descritti nella sezione [stili](common-control-styles.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 