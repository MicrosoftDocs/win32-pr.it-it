---
description: Proprio come un'applicazione richiede un contesto di dispositivo di visualizzazione (DC) prima di poter iniziare a disegnare nell'area client di una finestra, è necessario un controller di dominio della stampante prima che possa iniziare a inviare l'output a una stampante.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contesti di dispositivo stampante (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b75fb79d6ab8bb4198bf52bff10eccf5ec3cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231946"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contesti di dispositivo stampante (documenti e stampa)

Proprio come un'applicazione richiede un contesto di dispositivo di visualizzazione (DC) prima di poter iniziare a disegnare nell'area client di una finestra, è necessario un controller di dominio della stampante prima che possa iniziare a inviare l'output a una stampante. Un controller di dominio della stampante è simile a un controller di dominio di visualizzazione perché si tratta di una struttura di dati interna che definisce un set di oggetti grafici e i relativi attributi associati e specifica le modalità grafiche che interessano l'output. Gli oggetti grafici includono una penna per il disegno a linee, un pennello per il disegno e il riempimento e un tipo di carattere per l'output di testo.

Diversamente da un controller di dominio di visualizzazione, un controller di dominio della stampante non è di proprietà del componente di gestione della finestra e non può essere ottenuto chiamando la funzione [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) . Al contrario, un'applicazione deve chiamare la funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

Se l'applicazione chiama la funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , deve fornire un nome di driver e di porta. Per recuperare questi nomi, chiamare la funzione [**GetPrinter**](getprinter.md) o [**EnumPrinters**](enumprinters.md) .

Se l'applicazione chiama la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e specifica il \_ valore PD RETURNDC nel membro **Flags** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , il sistema restituisce un handle a un contesto di dispositivo per la stampante selezionata dall'utente. Per ulteriori informazioni, vedere finestra delle [proprietà di stampa](../dlgbox/print-property-sheet.md) e "utilizzo della finestra delle proprietà di stampa" in utilizzo di [finestre di dialogo comuni](../dlgbox/using-common-dialog-boxes.md).

 

 
