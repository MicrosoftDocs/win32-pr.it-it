---
description: Proprio come un'applicazione richiede un contesto di dispositivo di visualizzazione (DC) prima di poter iniziare a disegnare nell'area client di una finestra, è necessario un controller di dominio della stampante prima di poter iniziare a inviare l'output a una stampante.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contesti di dispositivo della stampante (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947401"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contesti di dispositivo della stampante (documenti e stampa)

Proprio come un'applicazione richiede un contesto di dispositivo di visualizzazione (DC) prima di poter iniziare a disegnare nell'area client di una finestra, è necessario un controller di dominio della stampante prima di poter iniziare a inviare l'output a una stampante. Un controller di dominio stampante è simile a un controller di dominio di visualizzazione in quanto è una struttura di dati interna che definisce un set di oggetti grafici e i relativi attributi associati e specifica le modalità grafiche che influiscono sull'output. Gli oggetti grafici includono una penna per il disegno a linee, un pennello per il disegno e il riempimento e un tipo di carattere per l'output di testo.

A differenza di un controller di dominio di visualizzazione, un controller di dominio della stampante non è di proprietà del componente di gestione delle finestre e non può essere ottenuto chiamando la [**funzione GetDC.**](/windows/desktop/api/winuser/nf-winuser-getdc) Un'applicazione deve invece chiamare la [**funzione CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o PrintDlgEx.**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))

Se l'applicazione chiama [**la funzione CreateDC,**](/windows/desktop/api/wingdi/nf-wingdi-createdca) deve fornire un driver e un nome di porta. Per recuperare questi nomi, chiamare la [**funzione GetPrinter**](getprinter.md) [**o EnumPrinters.**](enumprinters.md)

Se l'applicazione chiama la funzione [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e specifica il valore PD RETURNDC nel membro Flags della struttura \_ [**PRINTDLGEX,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) il sistema restituisce un handle a un contesto di dispositivo per la stampante selezionata dall'utente.  Per altre informazioni, vedere [Finestra delle proprietà Stampa](../dlgbox/print-property-sheet.md) e "Uso della finestra delle proprietà Stampa" in Uso di finestre di dialogo [comuni](../dlgbox/using-common-dialog-boxes.md).

 

 
