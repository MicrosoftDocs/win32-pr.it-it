---
description: A partire da Windows Vista, TextInputPanel sostituisce l'oggetto PenInputPanel per il controllo dell'aspetto e del comportamento sullo schermo del pannello di input del tablet. nelle sezioni seguenti viene descritto come programmare il pannello input utilizzando le interfacce di programmazione dell'applicazione Pannello di input di testo. TextInputPanel per gli utenti del pannello di input di PenInputPanelUsing AutoCompleteEnabling correzione del testo per l'input penna personalizzato CollectorsNote il pannello input di testo viene implementato in un file eseguibile denominato TabTip.exe. L'esecuzione di TabTip.exe con il parametro/SeekDesktop tenta di eseguire una versione ridotta della funzionalità del pannello di input in un desktop interattivo non standard, creato con CreateDesktop. Per la maggior parte dei desktop creati, il pannello di input verrà eseguito automaticamente in questa modalità. Questo parametro fornisce i mezzi per avviarlo in scenari di applicazione insoliti che altrimenti impediscano l'avvio automatico. Se il pannello input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmazione del pannello input di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318692"
---
# <a name="programming-the-text-input-panel"></a>Programmazione del pannello input di testo

A partire da Windows Vista, [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) sostituisce l'oggetto [**PenInputPanel**](peninputpanel-class.md) per il controllo dell'aspetto e del comportamento sullo schermo del pannello input penna.

Le sezioni seguenti descrivono la programmazione del pannello di input usando le interfacce di programmazione delle applicazioni del pannello input di testo.

-   [TextInputPanel per utenti di PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Uso del completamento automatico del pannello di input](using-input-panel-autocomplete.md)
-   [Abilitazione della correzione del testo per gli agenti di raccolta input penna personalizzati](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> Il pannello input di testo viene implementato in un file eseguibile denominato TabTip.exe. L'esecuzione di TabTip.exe con il parametro */SeekDesktop* tenta di eseguire una versione ridotta della funzionalità del pannello di input in un desktop interattivo non standard, creato con [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa). Per la maggior parte dei desktop creati, il pannello di input verrà eseguito automaticamente in questa modalità. Questo parametro fornisce i mezzi per avviarlo in scenari di applicazione insoliti che altrimenti impediscano l'avvio automatico. Se il pannello input è già in esecuzione sul desktop, questo parametro non avrà alcun effetto e l'istanza di TabTip.exe verrà chiusa immediatamente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione del pannello di input usando la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
