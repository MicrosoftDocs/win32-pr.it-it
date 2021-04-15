---
title: Flag di inizializzazione comuni della finestra di dialogo
description: I flag vengono utilizzati per modificare il comportamento e l'aspetto di una finestra di dialogo comune.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Libreria finestra di dialogo comune, inizializzazione
- finestre di dialogo comuni, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/19/2020
ms.locfileid: "104474729"
---
# <a name="common-dialog-box-initialization-flags"></a>Flag di inizializzazione comuni della finestra di dialogo

I flag vengono utilizzati per modificare il comportamento e l'aspetto di una finestra di dialogo comune. I flag di inizializzazione sono i valori impostati nel membro **Flags** della struttura utilizzata per creare la finestra di dialogo. Usare i flag per specificare i controlli in una finestra di dialogo che ricevono i valori iniziali, per disabilitare i controlli selezionati e per modificare l'intervallo di valori che l'utente può impostare con i controlli. È inoltre possibile utilizzare i flag per abilitare le procedure Hook e i modelli personalizzati per le finestre di dialogo.

Ad esempio, è possibile impostare il valore degli **\_ effetti CF** nel membro **flag** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per indicare alla finestra di dialogo **tipo di carattere** di visualizzare i controlli effetti. Questi controlli consentono all'utente di scegliere un colore del carattere, nonché gli effetti barrato e sottolineato.

I valori del flag di inizializzazione sono univoci per ogni finestra di dialogo comune e sono descritti in dettaglio dai membri dei **flag** delle seguenti strutture corrispondenti:

-   [**LE CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




