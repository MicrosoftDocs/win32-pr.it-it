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
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="785f5-103">Creazione di una connessione remota a Internet</span><span class="sxs-lookup"><span data-stu-id="785f5-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="785f5-104">Le funzioni seguenti vengono utilizzate per gestire le connessioni modem.</span><span class="sxs-lookup"><span data-stu-id="785f5-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="785f5-105">**InternetAutodial**</span><span class="sxs-lookup"><span data-stu-id="785f5-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="785f5-106">**InternetAutodialHangup**</span><span class="sxs-lookup"><span data-stu-id="785f5-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="785f5-107">**InternetDial**</span><span class="sxs-lookup"><span data-stu-id="785f5-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="785f5-108">**InternetGetConnectedState**</span><span class="sxs-lookup"><span data-stu-id="785f5-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="785f5-109">**InternetGetConnectedStateEx**</span><span class="sxs-lookup"><span data-stu-id="785f5-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="785f5-110">**InternetHangUp**</span><span class="sxs-lookup"><span data-stu-id="785f5-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="785f5-111">**InternetGoOnline**</span><span class="sxs-lookup"><span data-stu-id="785f5-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="785f5-112">Le funzioni remote di WinINet non supportano le connessioni a doppia connessione, l'autenticazione con smart card o le connessioni che richiedono la certificazione basata sul Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="785f5-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="785f5-113">A partire da Windows Vista e Windows Server 2008, le funzioni remote di WinINet utilizzano le [funzioni RAS](/windows/desktop/RRAS/remote-access-service-functions) per stabilire una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="785f5-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="785f5-114">WinINet supporta la funzionalità documentata nella funzione [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .</span><span class="sxs-lookup"><span data-stu-id="785f5-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="785f5-115">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="785f5-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="785f5-116">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="785f5-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="785f5-117">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="785f5-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 