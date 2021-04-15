---
title: Creazione di finestre e desktop
description: Il sistema crea automaticamente la stazione finestra interattiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337486"
---
# <a name="window-station-and-desktop-creation"></a>Creazione di finestre e desktop

Il sistema crea automaticamente la stazione finestra interattiva. Quando un utente interattivo esegue l'accesso, il sistema associa la stazione interattiva della finestra alla sessione di accesso dell'utente. Il sistema crea anche il desktop di input predefinito per la stazione finestra interattiva ( \\ impostazione predefinita WinSta0). I processi avviati dall'utente connesso sono associati al \\ desktop predefinito di WinSta0.

Un processo può utilizzare la funzione [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) per creare una nuova stazione di finestra e la funzione **CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) per creare un nuovo desktop. Il numero di desktop che è possibile creare è limitato dalle dimensioni dell'heap del desktop di sistema. Per ulteriori informazioni, vedere [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).

Quando un processo non interattivo, ad esempio un'applicazione di servizio, tenta di connettersi a una stazione di Windows e non esiste alcuna stazione di finestra per la sessione di accesso al processo, il sistema tenta di creare una stazione di finestra e un desktop per la sessione. Il nome della stazione di finestra creata è basato sull'identificatore della sessione di accesso e il desktop è denominato predefinito, come descritto di seguito:

-   Se un servizio è in esecuzione nel contesto di sicurezza dell'account LocalSystem ma non include l'attributo SERVICE \_ Interactive \_ Process, usa la finestra di Windows Station e desktop: Service-0x0-3e7 $ \\ default. Questa finestra non è interattiva, quindi il servizio non è in grado di visualizzare un'interfaccia utente. Inoltre, i processi creati dal servizio non possono visualizzare un'interfaccia utente.
-   Se il servizio è in esecuzione nel contesto di sicurezza di un account utente, il nome della stazione della finestra è basato sul servizio SID utente-0x *Z1* - *Z2*$, dove *Z1* è la parte superiore del SID di accesso e *Z2* è la parte inferiore del SID di accesso. Poiché un SID è univoco per la sessione di accesso, due servizi in esecuzione nello stesso contesto di sicurezza ricevono stazioni della finestra univoche. Queste stazioni della finestra non sono interattive.

L'elenco di controllo di accesso discrezionale (DACL) per la finestra stazione e il desktop include i seguenti diritti di accesso per l'account utente del servizio:

Stazione finestra:

<dl> \_ACCESSCLIPBOARD winsta  
\_ACCESSGLOBALATOMS winsta  
\_CREATEDESKTOP winsta  
\_EXITWINDOWS winsta  
\_diritti READATTRIBUTES winsta  
\_diritti standard \_ richiesti  
</dl>

Desktop:

<dl> \_CREATEMENU desktop  
\_CREATEWINDOW desktop  
\_enumerazione desktop  
\_HOOKCONTROL desktop  
\_READOBJECTS desktop  
\_WRITEOBJECTS desktop  
\_diritti standard \_ richiesti  
</dl>

 

 