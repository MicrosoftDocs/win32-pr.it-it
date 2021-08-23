---
description: È possibile usare Win32 \_ Process.Create per eseguire uno script o un'applicazione in un computer remoto. Tuttavia, per motivi di sicurezza, il processo non può essere interattivo. Quando win32 \_ Process.Create viene chiamato nel computer locale, il processo può essere interattivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Creazione di processi in modalità remota tramite WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152afa1dba2e745665526ca1628f2a80b8fc8a527d16abebc4b9082d4c5c4341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568851"
---
# <a name="creating-processes-remotely-using-wmi"></a>Creazione di processi in modalità remota tramite WMI

È possibile usare [**Win32 \_ Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) per eseguire uno script o un'applicazione in un computer remoto. Tuttavia, per motivi di sicurezza, il processo non può essere interattivo. Quando **win32 \_ Process.Create** viene chiamato nel computer locale, il processo può essere interattivo.

> [!WARNING]
> In questo argomento viene descritta la procedura generale per la creazione di un processo remoto con WMI. Se si sta semplicemente cercando di eseguire uno script in un sistema remoto, vedere Connessione [a WMI a](connecting-to-wmi-remotely-starting-with-vista.md)partire da Windows Vista o Connessione a WMI in un computer remoto tramite [Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Per informazioni più generali sulla comunicazione remota con PowerShell, vedere [Esecuzione di comandi remoti](https://technet.microsoft.com/library/dd819505.aspx).

 

Il processo remoto non ha un'interfaccia utente, ma è elencato nella Gestione attività **.** Un processo creato in locale può essere eseguito con qualsiasi account se l'account dispone dell'autorizzazione **Execute Method** per lo spazio dei \\ nomi cimv2 radice. Un processo creato in remoto può essere eseguito con qualsiasi account se l'account dispone delle autorizzazioni **Execute Method** e **Remote Enable** per root \\ cimv2. Le **autorizzazioni Execute Method** e Remote **Enable** sono impostate in Controllo WMI nel Pannello di controllo. Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).

È possibile usare [**Win32 \_ ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) per creare un processo interattivo in modalità remota. I processi avviati da **Win32 \_ ScheduledJob.Create** vengono tuttavia eseguiti con l'account LocalSystem che può conferire troppi privilegi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Connessione a una terza delega computer](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
