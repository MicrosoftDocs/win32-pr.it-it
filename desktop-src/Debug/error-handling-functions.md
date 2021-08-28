---
description: Le funzioni seguenti vengono usate con la gestione degli errori.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Funzioni di gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912761"
---
# <a name="error-handling-functions"></a>Funzioni di gestione degli errori

Le funzioni seguenti vengono usate con la gestione degli errori.



| Funzione                                                 | Descrizione                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Bip**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Genera toni semplici sull'altoparlante.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Acquisisce una traccia dello stack risalendo lo stack e registrando le informazioni per ogni frame.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Visualizza una finestra di messaggio e termina l'applicazione alla chiusura della finestra di messaggio.                                         |
| [**Flashwindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Fa lampeggiare la finestra specificata una volta.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Lampeggia la finestra specificata.                                                                                                 |
| [**Messaggio di formato**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Formatta una stringa di messaggio.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Recupera la modalità di errore per il processo corrente.                                                                             |
| [**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Recupera il valore dell'ultimo codice di errore del thread chiamante.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Recupera la modalità di errore per il thread chiamante.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Riproduce un suono waveform.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Cerca nelle tabelle delle funzioni attive una voce corrispondente al valore PC specificato.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Recupera il codice di errore di sistema corrispondente al codice di errore NT specificato.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Recupera l'indirizzo di base dell'immagine che contiene il valore PC specificato.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Avvia una rimozione dei frame di chiamata di routine.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Avvia una rimozione dei frame di chiamata di routine.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Avvia una rimozione dei frame di chiamata di routine.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Recupera il contesto di chiamata della funzione che precede il contesto della funzione specificato.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Controlla se il sistema gestirà i tipi specificati di errori gravi o se il processo li gestirà.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Imposta il codice dell'ultimo errore per il thread chiamante.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Imposta il codice dell'ultimo errore per il thread chiamante.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Controlla se il sistema gestirà i tipi specificati di errori gravi o se verranno gestiti dal thread chiamante. |



 

 

 
