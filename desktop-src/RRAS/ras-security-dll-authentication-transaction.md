---
title: Transazione di autenticazione DLL di sicurezza RAS
description: Windows NT/Windows server RAS 2000 chiama la funzione RasSecurityDialogBegin della DLL di sicurezza per avviare l'autenticazione di un utente remoto.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789477"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transazione di autenticazione DLL di sicurezza RAS

Windows NT/Windows server RAS 2000 chiama la funzione [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) della DLL di sicurezza per avviare l'autenticazione di un utente remoto. Il server RAS è bloccato e non può accettare altre chiamate fino al completamento **di RasSecurityDialogBegin.** Per questo motivo, **RasSecurityDialogBegin** deve copiare i parametri di input, creare un thread per eseguire l'autenticazione e restituire il più rapidamente possibile.

Il thread creato dalla DLL di sicurezza usa le funzioni [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) e [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per comunicare con il computer remoto. Queste funzioni non sono disponibili per l'importazione statica da qualsiasi libreria. Al contrario, la DLL di sicurezza deve usare [**le funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a queste funzioni in RASMAN.DLL.

Durante una transazione di autenticazione, la gestione connessione RAS nel computer remoto visualizza una finestra del terminale. Il thread della DLL di sicurezza chiama [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) per inviare un messaggio da visualizzare nella finestra del terminale. Il thread chiama quindi [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per ricevere l'input immesso dall'utente remoto nella finestra del terminale. Il thread può effettuare un numero qualsiasi di **chiamate RasSecurityDialogSend,** con ogni chiamata seguita da **una chiamata RasSecurityDialogReceive.** Dopo ogni chiamata a **RasSecurityDialogReceive,** il thread deve chiamare una delle funzioni di attesa, ad esempio [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), per attendere il completamento delle operazioni di invio e ricezione asincrone. Il server RAS segnala un oggetto evento quando l'operazione di ricezione è stata completata o quando è trascorso un intervallo di timeout facoltativo.

Al termine dell'autenticazione dell'utente remoto, il thread chiama la [**funzione RasSecurityDialogComplete.**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) Questa chiamata passa una [**struttura \_ SECURITY MESSAGE**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) contenente i risultati della transazione di autenticazione al server RAS. Il server RAS esegue quindi una sequenza di pulizia che include una chiamata alla funzione [**RasSecurityDialogEnd della**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) DLL. In questo modo la DLL di sicurezza può eseguire qualsiasi operazione di pulizia necessaria.

La DLL di sicurezza può chiamare la [**funzione RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) per recuperare informazioni sulla porta associata a una transazione di autenticazione. **RasSecurityDialogGetInfo** inserisce una struttura [**RAS \_ SECURITY \_ INFO**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) che indica lo stato dell'ultima chiamata [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) per la porta.

 

 