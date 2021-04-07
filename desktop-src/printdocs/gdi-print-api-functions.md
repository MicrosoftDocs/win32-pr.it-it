---
description: Funzioni API di stampa GDI
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: Funzioni API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881401"
---
# <a name="gdi-print-api-functions"></a>Funzioni API di stampa GDI

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | La funzione [**AbortDoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) arresta il processo di stampa corrente e cancella tutti gli elementi disegnati dopo l'ultima chiamata alla funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | La funzione [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) è una funzione di callback definita dall'applicazione usata con la funzione [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) . Viene chiamato quando un processo di stampa deve essere annullato durante lo spooling. Il tipo **AbortProc** definisce un puntatore a questa funzione di callback. **AbortProc** è un segnaposto per il nome della funzione definita dall'applicazione.<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | La funzione [**DeviceCapabilities**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera le funzionalità di un driver della stampante.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | La funzione [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) termina un processo di stampa.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | La funzione **EndPage** notifica al dispositivo che l'applicazione ha terminato la scrittura in una pagina. Questa funzione viene in genere usata per indicare al driver di dispositivo di passare a una nuova pagina.<br/>                                                                                                                                                                             |
| [**Carattere speciale di escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | consente a un'applicazione di accedere alle funzionalità del dispositivo definite dal sistema che non sono disponibili tramite GDI.<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | La funzione [**ExtEscape**](/windows/desktop/api/wingdi/nf-wingdi-extescape) consente a un'applicazione di accedere alle funzionalità del dispositivo che non sono disponibili tramite GDI.<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | La funzione [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md) determina se la finestra specificata è attualmente reindirizzata per la stampa.<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | La funzione [**PrintWindow**](/windows/desktop/api/winuser/nf-winuser-printwindow) copia una finestra visiva nel contesto di dispositivo specificato (DC), in genere un controller di dominio della stampante.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | La funzione [**SetAbortProc**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) imposta la funzione di interruzione definita dall'applicazione che consente l'annullamento di un processo di stampa durante lo spooling.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | La funzione [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) avvia un processo di stampa.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | La funzione [**Startpage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) prepara il driver della stampante affinché accetti i dati.<br/>                                                                                                                                                                                                                                                                             |



 

 

