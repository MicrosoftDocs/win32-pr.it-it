---
title: Transazione di autenticazione DLL di sicurezza RAS
description: Il server RAS Windows NT/Windows 2000 chiama la funzione RasSecurityDialogBegin della DLL di sicurezza per iniziare un'autenticazione di un utente remoto.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109f6ad5cd3d7b76e30db099a478ffaf562feb32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517043"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transazione di autenticazione DLL di sicurezza RAS

Il server RAS Windows NT/Windows 2000 chiama la funzione [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) della DLL di sicurezza per iniziare un'autenticazione di un utente remoto. Il server RAS è bloccato e non può accettare altre chiamate fino a quando non viene restituito **RasSecurityDialogBegin** . Per questo motivo, **RasSecurityDialogBegin** deve copiare i parametri di input, creare un thread per eseguire l'autenticazione e restituire il più rapidamente possibile.

Il thread creato dalla DLL di sicurezza utilizza le funzioni [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) e [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per comunicare con il computer remoto. Queste funzioni non sono disponibili per l'importazione statica da una libreria. Al contrario, la DLL di sicurezza deve usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a queste funzioni in RASMAN.DLL.

Durante una transazione di autenticazione, la gestione connessione RAS nel computer remoto Visualizza una finestra del terminale. Il thread della DLL di sicurezza chiama [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) per inviare un messaggio da visualizzare nella finestra del terminale. Il thread chiama quindi [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per ricevere l'input che l'utente remoto digita nella finestra del terminale. Il thread può effettuare un numero qualsiasi di chiamate **RasSecurityDialogSend** , con ogni chiamata seguita da una chiamata **RasSecurityDialogReceive** . Dopo ogni chiamata a **RasSecurityDialogReceive**, il thread deve chiamare una delle funzioni di attesa, ad esempio [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), per attendere il completamento delle operazioni di invio e ricezione asincrone. Il server RAS segnala un oggetto evento quando l'operazione di ricezione è stata completata o quando è trascorso un intervallo di timeout facoltativo.

Al termine dell'autenticazione dell'utente remoto da parte del thread, viene chiamata la funzione [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) . Questa chiamata passa una struttura dei [**\_ messaggi di sicurezza**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) contenente i risultati della transazione di autenticazione al server RAS. Il server RAS esegue quindi una sequenza di pulitura che include una chiamata alla funzione [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) della dll. In questo modo la DLL di sicurezza consente di eseguire tutte le operazioni di pulizia necessarie.

La DLL di sicurezza può chiamare la funzione [**RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) per recuperare le informazioni sulla porta associata a una transazione di autenticazione. **RasSecurityDialogGetInfo** compila una struttura di [**\_ \_ informazioni di sicurezza RAS**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) che indica lo stato dell'ultima chiamata [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per la porta.

 

 