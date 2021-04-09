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
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="e2f90-103">Funzioni di Servizi terminal GINA</span><span class="sxs-lookup"><span data-stu-id="e2f90-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="e2f90-104">Quando i servizi Terminal sono abilitati, [*Gina*](../secgloss/g-gly.md) deve chiamare le funzioni di supporto di [*Winlogon*](../secgloss/w-gly.md) per completare la configurazione di ogni utente, per eseguire una query sulle [*credenziali*](../secgloss/c-gly.md) di una sessione client di Servizi terminal e per disconnettersi da una sessione di rete di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="e2f90-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="e2f90-105">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2f90-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="e2f90-106">Di seguito sono riportate le funzioni di supporto.</span><span class="sxs-lookup"><span data-stu-id="e2f90-106">These support functions include the following.</span></span>



| <span data-ttu-id="e2f90-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="e2f90-107">Function</span></span>                                                                     | <span data-ttu-id="e2f90-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2f90-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2f90-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="e2f90-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="e2f90-110">Completa la configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e2f90-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="e2f90-111">**WlxQueryClientCredentials**</span><span class="sxs-lookup"><span data-stu-id="e2f90-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="e2f90-112">Chiamato per eseguire una query sulle credenziali dei client remoti che non utilizzano una licenza di Internet Connector.</span><span class="sxs-lookup"><span data-stu-id="e2f90-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="e2f90-113">**WlxQueryInetConnectorCredentials**</span><span class="sxs-lookup"><span data-stu-id="e2f90-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="e2f90-114">Chiamato per eseguire una query sulle credenziali dei client remoti che utilizzano una licenza di Internet Connector.</span><span class="sxs-lookup"><span data-stu-id="e2f90-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="e2f90-115">**WlxQueryTerminalServicesData**</span><span class="sxs-lookup"><span data-stu-id="e2f90-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="e2f90-116">Chiamata eseguita per recuperare le informazioni di configurazione dell'utente di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="e2f90-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="e2f90-117">**WlxDisconnect**</span><span class="sxs-lookup"><span data-stu-id="e2f90-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="e2f90-118">Chiamato per disconnettersi da una sessione di rete di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="e2f90-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="e2f90-119">Per accedere alle funzioni di supporto di Winlogon, la DLL GINA deve usare la struttura [**wlx \_ Dispatch \_ versione \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) .</span><span class="sxs-lookup"><span data-stu-id="e2f90-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="e2f90-120">Nella funzione [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) di Gina, entrambi i parametri devono essere almeno wlx \_ versione \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="e2f90-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
