---
title: Funzioni di Window Station e Desktop
description: Le applicazioni possono usare le funzioni seguenti con oggetti stazione finestra.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810401"
---
# <a name="window-station-and-desktop-functions"></a>Funzioni di Window Station e Desktop

Le applicazioni possono usare le funzioni seguenti con [oggetti stazione finestra.](window-stations.md)



| Funzione                                                     | Descrizione                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Chiude un handle di stazione finestra aperto.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Crea un oggetto stazione finestra, lo associa al processo corrente e lo assegna alla sessione corrente. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Enumera tutte le stazioni finestra nella sessione corrente.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Recupera un handle per la stazione della finestra corrente per il processo chiamante.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Recupera informazioni sulla stazione della finestra o sull'oggetto desktop specificato.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Recupera le informazioni di sicurezza per la stazione finestra o l'oggetto desktop specificato.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Apre la stazione della finestra specificata.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Assegna la stazione finestra specificata al processo chiamante.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Imposta informazioni sulla stazione della finestra o sull'oggetto desktop specificato.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Imposta le informazioni di sicurezza per la stazione finestra o l'oggetto desktop specificato.                                   |



 

Le applicazioni possono usare le funzioni seguenti con gli [oggetti desktop.](desktops.md)



| Funzione                                                     | Descrizione                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Chiude un handle aperto a un oggetto desktop.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Crea un nuovo desktop, lo associa alla finestra corrente del processo chiamante e lo assegna al thread chiamante. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Crea un nuovo desktop, lo associa alla finestra corrente del processo chiamante e lo assegna al thread chiamante. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Enumera tutti i desktop associati alla stazione finestra corrente del processo chiamante.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Enumera tutte le finestre di primo livello associate al desktop specificato.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Recupera un handle per il desktop assegnato al thread specificato.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Ottiene informazioni su una stazione finestra o un oggetto desktop.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Ottiene le informazioni di sicurezza per una stazione finestra o un oggetto desktop.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Apre l'oggetto desktop specificato.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Apre il desktop che riceve l'input dell'utente.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Assegna il desktop specificato al thread chiamante.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Imposta informazioni su una stazione finestra o un oggetto desktop.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Imposta le informazioni di sicurezza per una stazione finestra o un oggetto desktop.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Rende visibile un desktop e lo attiva. In questo modo il desktop può ricevere l'input dall'utente.                                 |



 

 

 