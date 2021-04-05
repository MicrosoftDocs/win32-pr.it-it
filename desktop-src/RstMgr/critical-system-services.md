---
title: Servizi di sistema critici
description: I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema. Gli aggiornamenti a qualsiasi file o risorsa in uso da parte di uno di questi servizi richiedono un riavvio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045407"
---
# <a name="critical-system-services"></a><span data-ttu-id="a3423-104">Servizi di sistema critici</span><span class="sxs-lookup"><span data-stu-id="a3423-104">Critical System Services</span></span>

<span data-ttu-id="a3423-105">I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3423-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="a3423-106">Gli aggiornamenti a qualsiasi file o risorsa in uso da parte di uno di questi servizi richiedono un riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3423-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="a3423-107">**Per determinare se un processo è un servizio di sistema critico.**</span><span class="sxs-lookup"><span data-stu-id="a3423-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="a3423-108">Registrare il processo utilizzando la funzione [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .</span><span class="sxs-lookup"><span data-stu-id="a3423-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="a3423-109">Chiamare la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) per ottenere la struttura delle [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .</span><span class="sxs-lookup"><span data-stu-id="a3423-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="a3423-110">Il membro **ApplicationType** della struttura di [**\_ \_ informazioni del processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) restituito contiene un valore di enumerazione del [**\_ \_ tipo di app RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="a3423-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="a3423-111">Questo valore è impostato su **RmCriticial** per un processo di sistema critico.</span><span class="sxs-lookup"><span data-stu-id="a3423-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="a3423-112">I servizi di sistema critici includono smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe con RPCSS e svchost.exe con DCOM/PnP.</span><span class="sxs-lookup"><span data-stu-id="a3423-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




