---
description: A partire da Windows Vista, TextInputPanel sostituisce PenInputPanel per controllare l'aspetto e il comportamento sullo schermo del pannello input tablet. Le sezioni seguenti descrivono la programmazione del pannello di input usando le interfacce di programmazione dell'applicazione Pannello input di testo. TextInputPanel for Users of PenInputPanelUsing Input Panel AutoComplete (TextInputPanel per gli utenti di PenInputPanelutilizzo del completamento automatico del pannello di input) Correzione del testo per gli agenti di raccolta input penna personalizzatiNota che il pannello input penna viene implementato in un file eseguibile denominato TabTip.exe. LTabTip.exe con il parametro /SeekDesktop tenta di eseguire una versione con funzionalità ridotte del Pannello input penna in un desktop interattivo non standard, come creato con CreateDesktop. Per la maggior parte dei desktop creati, il Pannello di input verrà già eseguito automaticamente in questa modalità. Questo parametro consente di avviarlo in scenari applicativi insoliti che altrimenti impediscono l'avvio automatico. Se il pannello di input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmazione del pannello input di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366eb0a0d1770291ba2251247364fb68e14789d19fa053800ecaeec5ef4652d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716125"
---
# <a name="programming-the-text-input-panel"></a>Programmazione del pannello input di testo

A partire Windows Vista, [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) sostituisce [**PenInputPanel**](peninputpanel-class.md) per controllare l'aspetto e il comportamento sullo schermo del pannello di input del tablet.

Le sezioni seguenti descrivono la programmazione del Pannello di input usando le interfacce di programmazione dell'applicazione Pannello input di testo.

-   [TextInputPanel per gli utenti di PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Uso del completamento automatico del pannello di input](using-input-panel-autocomplete.md)
-   [Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> Il pannello input di testo viene implementato in un file eseguibile denominato TabTip.exe. LTabTip.exe con il *parametro /SeekDesktop* tenta di eseguire una versione con funzionalità ridotte del Pannello di input in un desktop interattivo non standard, come creato con [**CreateDesktop.**](/windows/win32/api/winuser/nf-winuser-createdesktopa) Per la maggior parte dei desktop creati, il Pannello di input verrà già eseguito automaticamente in questa modalità. Questo parametro consente di avviarlo in scenari applicativi insoliti che altrimenti impediscono l'avvio automatico. Se il pannello di input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione del pannello di input con la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
