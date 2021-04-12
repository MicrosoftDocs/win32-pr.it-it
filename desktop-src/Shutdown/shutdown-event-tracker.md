---
description: L'individuazione evento di arresto consente all'utente o all'applicazione di documentare il motivo dell'arresto o del riavvio del sistema.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Individuazione evento di arresto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345706"
---
# <a name="shutdown-event-tracker"></a>Individuazione evento di arresto

L' *Individuazione evento di arresto* consente all'utente o all'applicazione di documentare il motivo dell'arresto o del riavvio del sistema. All'utente viene richiesto di immettere informazioni quando si seleziona **Arresta** dal menu **Start** o quando si usa Shutdown.exe. Gli sviluppatori possono includere un codice motivo quando chiamano le funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) . Le informazioni vengono archiviate nel registro eventi.

**Windows XP:** Questa funzionalità è abilitata per impostazione predefinita a partire da Windows Server 2003, quindi è necessario abilitarla in Windows XP. Per ulteriori informazioni, vedere la documentazione relativa a Shutdown Event Tracker incluso nel sistema o in TechNet.

Le funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) sono state aggiornate per supportare i codici motivo di arresto nel parametro *dwReason* . Usare i valori definiti in Reason. h per costruire un codice motivo di arresto oppure definire un codice motivo personalizzato. Il codice motivo di arresto viene creato da un flag principale, un flag secondario e due flag facoltativi. Per ulteriori informazioni, vedere [codici motivo dell'arresto del sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione evento di arresto (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
