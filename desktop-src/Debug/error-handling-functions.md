---
description: Le funzioni seguenti vengono utilizzate con la gestione degli errori.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Funzioni di gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4cea391f05638310e17b9ef283e138204bc2cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125727"
---
# <a name="error-handling-functions"></a>Funzioni di gestione degli errori

Le funzioni seguenti vengono utilizzate con la gestione degli errori.



| Funzione                                                 | Descrizione                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Segnale acustico**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Genera toni semplici nell'altoparlante.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Acquisisce una traccia dello stack indietro scorrendo lo stack e registrando le informazioni per ogni fotogramma.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Visualizza una finestra di messaggio e termina l'applicazione quando la finestra di messaggio viene chiusa.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Lampeggia la finestra specificata una volta.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Lampeggia la finestra specificata.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Formatta una stringa di messaggio.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Recupera la modalità di errore per il processo corrente.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Recupera il valore del codice dell'ultimo errore del thread chiamante.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Recupera la modalità di errore per il thread chiamante.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Riproduce un suono di forma d'onda.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Cerca nella tabella delle funzioni attive una voce che corrisponde al valore del PC specificato.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Recupera il codice di errore del sistema che corrisponde al codice di errore NT specificato.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Recupera l'indirizzo di base dell'immagine che contiene il valore del PC specificato.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Avvia una rimozione dei frame di chiamata di procedura.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Avvia una rimozione dei frame di chiamata di procedura.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Avvia una rimozione dei frame di chiamata di procedura.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Recupera il contesto di chiamata della funzione che precede il contesto della funzione specificato.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Controlla se il sistema gestirà i tipi specificati di errori gravi o se tali errori vengono gestiti dal processo.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Imposta il codice dell'ultimo errore per il thread chiamante.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Imposta il codice dell'ultimo errore per il thread chiamante.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Controlla se il sistema gestirà i tipi specificati di errori gravi o se il thread chiamante lo gestirà. |



 

 

 
