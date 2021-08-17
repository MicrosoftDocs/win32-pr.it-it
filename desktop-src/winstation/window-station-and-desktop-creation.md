---
title: Creazione di window station e desktop
description: Il sistema crea automaticamente la stazione finestra interattiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52a3cc85a3194bea6c8eaea00a7ce794901426e794c962e1b23713561f8fc744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030517"
---
# <a name="window-station-and-desktop-creation"></a>Creazione di window station e desktop

Il sistema crea automaticamente la stazione finestra interattiva. Quando un utente interattivo accede, il sistema associa la stazione finestra interattiva alla sessione di accesso dell'utente. Il sistema crea anche il desktop di input predefinito per la stazione finestra interattiva (impostazione predefinita \\ Winsta0). I processi avviati dall'utente connesso sono associati al desktop predefinito \\ Winsta0.

Un processo può usare la [**funzione CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) per creare una nuova stazione finestra e la funzione **CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) per creare un nuovo desktop. Il numero di desktop che è possibile creare è limitato dalle dimensioni dell'heap del desktop di sistema. Per altre informazioni, vedere [**CreateDesktop.**](/windows/win32/api/winuser/nf-winuser-createdesktopa)

Quando un processo non interattivo, ad esempio un'applicazione di servizio, tenta di connettersi a una stazione finestra e non esiste alcuna stazione finestra per la sessione di accesso al processo, il sistema tenta di creare una stazione finestra e un desktop per la sessione. Il nome della stazione finestra creata è basato sull'identificatore della sessione di accesso e il desktop è denominato default, come descritto di seguito:

-   Se un servizio è in esecuzione nel contesto di sicurezza dell'account LocalSystem ma non include l'attributo SERVICE INTERACTIVE PROCESS, usa l'impostazione predefinita \_ \_ Service-0x0-3e7$. \\ Questa stazione finestra non è interattiva, quindi il servizio non può visualizzare un'interfaccia utente. Inoltre, i processi creati dal servizio non possono visualizzare un'interfaccia utente.
-   Se il servizio è in esecuzione nel contesto di sicurezza di un account utente, il nome della stazione finestra è basato sul SID utente Service-0x *Z1* - *Z2*$, dove *Z1* è la parte superiore del SID di accesso e *Z2* è la parte inferiore del SID di accesso. Poiché un SID è univoco per la sessione di accesso, due servizi in esecuzione nello stesso contesto di sicurezza ricevono stazioni finestra univoche. Queste stazioni finestra non sono interattive.

L'elenco di controllo di accesso discrezionale (DACL) per la stazione finestra e il desktop include i diritti di accesso seguenti per l'account utente del servizio:

Stazione finestra:

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
DIRITTI \_ STANDARD \_ RICHIESTI  
</dl>

Desktop:

<dl> DESKTOP \_ CREATEMENU  
DESKTOP \_ CREATEWINDOW  
ENUMERAZIONE \_ DESKTOP  
DESKTOP \_ HOOKCONTROL  
OGGETTI \_ READOBJECT DESKTOP  
\_WRITEOBJECT DESKTOP  
DIRITTI \_ STANDARD \_ RICHIESTI  
</dl>

 

 