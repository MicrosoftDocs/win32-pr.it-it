---
description: Quando Servizi terminal è abilitato, l'APPLICAZIONE deve chiamare le funzioni di supporto winlogon per completare la configurazione per ogni utente, per eseguire query sulle credenziali di una sessione client di Servizi terminal e per disconnettersi da una sessione di rete di Servizi terminal. Si noti che le DLL DELL'APPLICAZIONE vengono ignorate in Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Funzioni DISA di Servizi terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bdd81d66d88ae280c14d71d7d65385c0d5580b3e28cef9d0f26ed1963bded1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916393"
---
# <a name="terminal-services-gina-functions"></a>Funzioni DISA di Servizi terminal

Quando Servizi terminal è abilitato, [*l'APPLICAZIONE*](../secgloss/g-gly.md) deve chiamare le funzioni di supporto [](../secgloss/c-gly.md) [*winlogon*](../secgloss/w-gly.md) per completare la configurazione per ogni utente, per eseguire query sulle credenziali di una sessione client di Servizi terminal e per disconnettersi da una sessione di rete di Servizi terminal.

> [!Note]  
> Le DLL DELL'APPLICAZIONE vengono ignorate in Windows Vista.

 

Queste funzioni di supporto includono quanto segue.



| Funzione                                                                     | Descrizione                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Completa la configurazione dell'utente.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Chiamato per eseguire una query sulle credenziali dei client remoti che non usano una licenza del connettore Internet. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Chiamato per eseguire una query sulle credenziali dei client remoti che usano una licenza del connettore Internet.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Chiamato per recuperare le informazioni di configurazione utente di Servizi terminal.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Chiamato per disconnettersi da una sessione di rete di Servizi terminal.                                      |



 

Per accedere a queste funzioni di supporto winlogon, la DLL DELL'APPLICAZIONE DEVE usare la [**struttura WLX \_ DISPATCH \_ VERSION \_ 1 \_ 3.**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) Nella funzione [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) di DELLA entrambi i parametri devono essere almeno WLX \_ VERSION \_ 1 \_ 3.

 

 
