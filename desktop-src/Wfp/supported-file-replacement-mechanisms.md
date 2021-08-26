---
description: La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Meccanismi di sostituzione delle risorse supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8f839e65ddd07bbde6bb4e089c3235ee6930dec910c07c1c318e666b034afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999251"
---
# <a name="supported-resource-replacement-mechanisms"></a>Meccanismi di sostituzione delle risorse supportati

La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.

L'autorizzazione per l'accesso completo per modificare le risorse protette da WRP in Windows Vista e Windows Server 2008 è limitata a TrustedInstaller con il servizio Windows Modules Installer usando i meccanismi seguenti:

-   Windows Service Pack installati da TrustedInstaller.
-   Hotfix installati da TrustedInstaller.
-   Aggiornamenti del sistema operativo installati da TrustedInstaller.
-   Windows Aggiornamento installato da TrustedInstaller.

Alle applicazioni e ai programmi di installazione che tentano di sostituire una risorsa protetta da WRP con mezzi diversi da questi metodi specificati viene negato l'accesso per modificare la risorsa e generare un messaggio di errore di accesso negato.

Per i programmi di installazione noti che tentano di sostituire le risorse protette da WRP, l'errore di accesso negato e il messaggio di errore potrebbero essere eliminati. In questo caso, l'operazione viene restituita correttamente, l'errore e il messaggio di errore vengono eliminati, ma non vengono applicate modifiche alla risorsa protetta da WRP. L'errore può essere eliminato per un programma di installazione noto solo quando vengono soddisfatti tutti i criteri seguenti:

-   Si tratta di un'applicazione legacy. L'applicazione non include un manifesto con requestedExecutionlevel che identifica l'applicazione come progettata per Windows Vista o Windows Server 2008.
-   L'errore di accesso negato è causato solo dal tentativo di modificare una risorsa protetta da WRP.
-   Un amministratore sta installando l'applicazione.

Per informazioni sull'uso del Windows Installer con WRP, vedere Using [Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in Windows [Installer](/windows/desktop/Msi/windows-installer-portal) SDK.

**Windows Server 2003 e Windows XP:** La sostituzione dei file di sistema protetti da WFP è supportata solo tramite i meccanismi seguenti:

-   Windows Installazione del Service Pack tramite Update.exe
-   Hotfix installati tramite Hotfix.exe
-   Aggiornamenti del sistema operativo con Winnt32.exe
-   Windows Update

La sostituzione dei file protetti con mezzi diversi da questi metodi specificati comporta il ripristino dei file originali da parte del WFP.

 

 
