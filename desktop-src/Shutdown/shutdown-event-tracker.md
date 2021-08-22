---
description: Shutdown Event Tracker consente all'utente o all'applicazione di documentare il motivo dell'arresto o del riavvio del sistema.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Individuazione evento di arresto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2deaebde736ed2e0ba72f38e8849cf815b167da68fdddbecb92e713083699b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664361"
---
# <a name="shutdown-event-tracker"></a>Individuazione evento di arresto

Shutdown *Event Tracker consente* all'utente o all'applicazione di documentare il motivo dell'arresto o del riavvio del sistema. All'utente viene richiesto di immettere le informazioni quando **si** seleziona Arresta dal menu **Start** o quando si usa Shutdown.exe. Gli sviluppatori possono includere un codice motivo quando chiamano [**le funzioni ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) [**e InitiateSystemShutdownEx.**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) Le informazioni vengono archiviate nel registro eventi.

**Windows XP:** Anche se questa funzionalità è abilitata per impostazione predefinita a partire da Windows Server 2003, è necessario abilitarla in Windows XP. Per altre informazioni, vedere la documentazione relativa a Shutdown Event Tracker incluso nel sistema o in TechNet.

Le [**funzioni ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) sono state aggiornate per supportare i codici motivo dell'arresto nel *parametro dwReason.* Usare i valori definiti in Reason.h per costruire un codice motivo di arresto o definire un codice motivo personalizzato. Un codice motivo di arresto viene costruito da un flag principale, un flag secondario e due flag facoltativi. Per altre informazioni, vedere Codici [motivo dell'arresto del sistema.](system-shutdown-reason-codes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
