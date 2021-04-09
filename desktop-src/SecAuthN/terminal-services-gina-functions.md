---
description: Quando i servizi Terminal sono abilitati, GINA deve chiamare le funzioni di supporto di Winlogon per completare la configurazione di ogni utente, per eseguire una query sulle credenziali di una sessione client di Servizi terminal e per disconnettersi da una sessione di rete di Servizi terminal. Nota le DLL GINA vengono ignorate in Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Funzioni di Servizi terminal GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879042"
---
# <a name="terminal-services-gina-functions"></a>Funzioni di Servizi terminal GINA

Quando i servizi Terminal sono abilitati, [*Gina*](../secgloss/g-gly.md) deve chiamare le funzioni di supporto di [*Winlogon*](../secgloss/w-gly.md) per completare la configurazione di ogni utente, per eseguire una query sulle [*credenziali*](../secgloss/c-gly.md) di una sessione client di Servizi terminal e per disconnettersi da una sessione di rete di Servizi terminal.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Di seguito sono riportate le funzioni di supporto.



| Funzione                                                                     | Descrizione                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Completa la configurazione dell'utente.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Chiamato per eseguire una query sulle credenziali dei client remoti che non utilizzano una licenza di Internet Connector. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Chiamato per eseguire una query sulle credenziali dei client remoti che utilizzano una licenza di Internet Connector.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Chiamata eseguita per recuperare le informazioni di configurazione dell'utente di Servizi terminal.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Chiamato per disconnettersi da una sessione di rete di Servizi terminal.                                      |



 

Per accedere alle funzioni di supporto di Winlogon, la DLL GINA deve usare la struttura [**wlx \_ Dispatch \_ versione \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) . Nella funzione [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) di Gina, entrambi i parametri devono essere almeno wlx \_ versione \_ 1 \_ 3.

 

 
