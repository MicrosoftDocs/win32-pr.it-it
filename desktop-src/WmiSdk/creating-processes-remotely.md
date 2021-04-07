---
description: È possibile utilizzare Win32 \_ Process. create per eseguire uno script o un'applicazione in un computer remoto. Tuttavia, per motivi di sicurezza, il processo non può essere interattivo. Quando Win32 \_ Process. Create viene chiamato sul computer locale, il processo può essere interattivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Creazione di processi in modalità remota tramite WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758747"
---
# <a name="creating-processes-remotely-using-wmi"></a>Creazione di processi in modalità remota tramite WMI

È possibile utilizzare [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) per eseguire uno script o un'applicazione in un computer remoto. Tuttavia, per motivi di sicurezza, il processo non può essere interattivo. Quando **Win32 \_ Process. Create** viene chiamato sul computer locale, il processo può essere interattivo.

> [!WARNING]
> In questo argomento viene descritta la procedura generale per la creazione di un processo remoto con WMI. Se si sta semplicemente cercando di eseguire uno script in un sistema remoto, vedere [connessione a WMI in modalità remota a partire da Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)o [connessione a WMI in un computer remoto tramite Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Per informazioni più generali sulla comunicazione remota con PowerShell, vedere [esecuzione di comandi remoti](https://technet.microsoft.com/library/dd819505.aspx).

 

Il processo remoto non dispone di alcuna interfaccia utente, ma è elencato in **Gestione attività**. Un processo creato localmente può essere eseguito con qualsiasi account se l'account dispone dell'autorizzazione **Execute Method** per lo \\ spazio dei nomi CIMV2 radice. Un processo creato in modalità remota può essere eseguito con qualsiasi account se l'account dispone delle autorizzazioni **Esegui metodo** e **Abilita remoto** per \\ CIMV2 radice. Le autorizzazioni **Execute Method** e **Remote Enable** sono impostate nel controllo WMI nel pannello di controllo. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).

È possibile utilizzare [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) per creare un processo interattivo in modalità remota. Ma i processi avviati da **Win32 \_ ScheduledJob. Create** vengono eseguiti con l'account LocalSystem che può conferire un privilegio troppo elevato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Connessione a un terzo computer-delega](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
