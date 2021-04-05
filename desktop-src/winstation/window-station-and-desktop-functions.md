---
title: Funzioni di Window Station e desktop
description: Le applicazioni possono utilizzare le seguenti funzioni con gli oggetti Window Station.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6665f52de1f7f57930105edb0063c4512e375ac3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727354"
---
# <a name="window-station-and-desktop-functions"></a>Funzioni di Window Station e desktop

Le applicazioni possono utilizzare le seguenti funzioni con gli oggetti [Window Station](window-stations.md) .



| Funzione                                                     | Descrizione                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Chiude un handle della stazione della finestra aperta.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Crea un oggetto della stazione della finestra, lo associa al processo corrente e lo assegna alla sessione corrente. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Enumera tutte le stazioni della finestra nella sessione corrente.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Recupera un handle per la stazione di finestra corrente per il processo chiamante.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Recupera le informazioni sulla stazione di finestra o sull'oggetto desktop specificato.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Recupera le informazioni di sicurezza per la stazione di finestra o l'oggetto desktop specificato.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Apre la stazione della finestra specificata.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Assegna la stazione della finestra specificata al processo chiamante.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Imposta le informazioni sulla stazione di finestra o sull'oggetto desktop specificato.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Imposta le informazioni di sicurezza per l'oggetto Window Station o desktop specificato.                                   |



 

Le applicazioni possono utilizzare le seguenti funzioni con oggetti [Desktop](desktops.md) .



| Funzione                                                     | Descrizione                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Chiude un handle aperto per un oggetto desktop.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Crea un nuovo desktop, lo associa alla stazione della finestra corrente del processo chiamante e lo assegna al thread chiamante. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Crea un nuovo desktop, lo associa alla stazione della finestra corrente del processo chiamante e lo assegna al thread chiamante. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Enumera tutti i desktop associati alla stazione della finestra corrente del processo chiamante.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Enumera tutte le finestre di primo livello associate al desktop specificato.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Recupera un handle per il desktop assegnato al thread specificato.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ottiene informazioni su una stazione di finestra o un oggetto desktop.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ottiene le informazioni sulla sicurezza per un oggetto Window Station o desktop.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Apre l'oggetto desktop specificato.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Apre il desktop che riceve l'input dell'utente.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Assegna il desktop specificato al thread chiamante.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Imposta le informazioni relative a una stazione di finestra o un oggetto desktop.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Imposta le informazioni di sicurezza per un oggetto Window Station o desktop.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Rende visibile un desktop e lo attiva. Ciò consente al desktop di ricevere l'input dall'utente.                                 |



 

 

 