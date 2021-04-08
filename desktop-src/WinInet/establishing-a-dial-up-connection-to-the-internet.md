---
title: Creazione di una connessione remota a Internet
description: Le funzioni seguenti vengono utilizzate per gestire le connessioni modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047226"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Creazione di una connessione remota a Internet

Le funzioni seguenti vengono utilizzate per gestire le connessioni modem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Le funzioni remote di WinINet non supportano le connessioni a doppia connessione, l'autenticazione con smart card o le connessioni che richiedono la certificazione basata sul Registro di sistema.

 

> [!Note]  
> A partire da Windows Vista e Windows Server 2008, le funzioni remote di WinINet utilizzano le [funzioni RAS](/windows/desktop/RRAS/remote-access-service-functions) per stabilire una connessione remota. WinINet supporta la funzionalità documentata nella funzione [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 