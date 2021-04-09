---
title: Funzioni di ripristino e riavvio dell'applicazione
description: Il ripristino e il riavvio dell'applicazione definiscono le funzioni seguenti
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118146"
---
# <a name="application-recovery-and-restart-functions"></a>Funzioni di ripristino e riavvio dell'applicazione

Il ripristino e il riavvio dell'applicazione definiscono le funzioni seguenti:



| Funzione                                                                               | Descrizione                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indica che l'applicazione chiamante ha completato il ripristino dei dati.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indica che l'applicazione chiamante sta continuando a ripristinare i dati.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Recupera un puntatore alla routine di callback di ripristino registrata per il processo specificato. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Recupera le informazioni di riavvio registrate per il processo specificato.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Registra l'istanza attiva di un'applicazione per il ripristino.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Registra l'istanza attiva di un'applicazione per il riavvio.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Consente di rimuovere l'istanza attiva di un'applicazione dall'elenco di ripristino.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Rimuove l'istanza attiva di un'applicazione dall'elenco di riavvio.                       |



 

 

 