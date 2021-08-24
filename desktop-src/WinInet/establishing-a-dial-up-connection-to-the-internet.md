---
title: Stabilire una connessione remota a Internet
description: Le funzioni seguenti vengono usate per gestire le connessioni modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955591"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Stabilire una connessione remota a Internet

Le funzioni seguenti vengono usate per gestire le connessioni modem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Le funzioni di connessione remota WinINet non supportano le connessioni a doppia connessione, l'autenticazione con smart card o le connessioni che richiedono la certificazione basata sul Registro di sistema.

 

> [!Note]  
> A partire da Windows Vista e Windows Server 2008, le funzioni di connessione remota WinINet usano le funzioni [RAS](/windows/desktop/RRAS/remote-access-service-functions) per stabilire una connessione remota. WinINet supporta la funzionalità documentata nella [**funzione RasDialDlg.**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga)

 

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 