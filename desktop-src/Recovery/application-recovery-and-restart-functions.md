---
title: Funzioni di ripristino e riavvio dell'applicazione
description: Application Recovery and Restart definisce le funzioni seguenti
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024621"
---
# <a name="application-recovery-and-restart-functions"></a>Funzioni di ripristino e riavvio dell'applicazione

Application Recovery and Restart definisce le funzioni seguenti:



| Funzione                                                                               | Descrizione                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica che l'applicazione chiamante ha completato il recupero dei dati.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica che l'applicazione chiamante sta continuando a recuperare i dati.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera un puntatore alla routine di callback di recupero registrata per il processo specificato. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera le informazioni di riavvio registrate per il processo specificato.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra l'istanza attiva di un'applicazione per il ripristino.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra l'istanza attiva di un'applicazione per il riavvio.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Rimuove l'istanza attiva di un'applicazione dall'elenco di ripristino.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Rimuove l'istanza attiva di un'applicazione dall'elenco di riavvio.                       |



 

 

 