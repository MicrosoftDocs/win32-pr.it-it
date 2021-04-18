---
description: La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Meccanismi di sostituzione delle risorse supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317022"
---
# <a name="supported-resource-replacement-mechanisms"></a>Meccanismi di sostituzione delle risorse supportati

La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.

L'autorizzazione per l'accesso completo per la modifica di risorse protette da WRP in Windows Vista e Windows Server 2008 è limitata a TrustedInstaller con il servizio Windows Modules Installer usando i meccanismi seguenti:

-   Service Pack di Windows installati da TrustedInstaller.
-   Aggiornamenti rapidi installati da TrustedInstaller.
-   Aggiornamenti del sistema operativo installati da TrustedInstaller.
-   Windows Update installato da TrustedInstaller.

Le applicazioni e i programmi di installazione che tentano di sostituire una risorsa protetta da WRP per mezzo di questi metodi vengono negati per modificare la risorsa e generare un messaggio di errore di accesso negato.

Per i programmi di installazione noti che tentano di sostituire le risorse protette con WRP, l'errore di accesso negato e il messaggio di errore possono essere eliminati. In questo caso, l'operazione viene restituita correttamente, i messaggi di errore e di errore vengono eliminati, ma non vengono applicate modifiche alla risorsa protetta da WRP. È possibile che l'errore venga eliminato per un programma di installazione noto solo quando vengono soddisfatti tutti i criteri seguenti:

-   Si tratta di un'applicazione legacy. L'applicazione non include un manifesto con un requestedExecutionlevel che identifica l'applicazione come progettata per Windows Vista o Windows Server 2008.
-   L'errore di accesso negato è causato solo dal tentativo di modificare una risorsa protetta da WRP.
-   L'applicazione viene installata da un amministratore.

Per informazioni sull'uso della Windows Installer con WRP, vedere [uso di Windows Installer e protezione risorse di Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.

**Windows Server 2003 e Windows XP:** La sostituzione dei file di sistema protetti da WFP è supportata solo tramite i meccanismi seguenti:

-   Installazione del Service Pack di Windows con Update.exe
-   Hotfix installati con Hotfix.exe
-   Aggiornamenti del sistema operativo con Winnt32.exe
-   Windows Update

La sostituzione dei file protetti per mezzo di questi metodi diversi comporta l'esecuzione del ripristino dei file originali da parte di WFP.

 

 
