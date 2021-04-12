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
# <a name="shutdown-event-tracker"></a><span data-ttu-id="a0b39-103">Individuazione evento di arresto</span><span class="sxs-lookup"><span data-stu-id="a0b39-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="a0b39-104">L' *Individuazione evento di arresto* consente all'utente o all'applicazione di documentare il motivo dell'arresto o del riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0b39-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="a0b39-105">All'utente viene richiesto di immettere informazioni quando si seleziona **Arresta** dal menu **Start** o quando si usa Shutdown.exe.</span><span class="sxs-lookup"><span data-stu-id="a0b39-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="a0b39-106">Gli sviluppatori possono includere un codice motivo quando chiamano le funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .</span><span class="sxs-lookup"><span data-stu-id="a0b39-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="a0b39-107">Le informazioni vengono archiviate nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="a0b39-107">The information is stored in the event log.</span></span>

<span data-ttu-id="a0b39-108">**Windows XP:** Questa funzionalità è abilitata per impostazione predefinita a partire da Windows Server 2003, quindi è necessario abilitarla in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0b39-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="a0b39-109">Per ulteriori informazioni, vedere la documentazione relativa a Shutdown Event Tracker incluso nel sistema o in TechNet.</span><span class="sxs-lookup"><span data-stu-id="a0b39-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="a0b39-110">Le funzioni [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) sono state aggiornate per supportare i codici motivo di arresto nel parametro *dwReason* .</span><span class="sxs-lookup"><span data-stu-id="a0b39-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="a0b39-111">Usare i valori definiti in Reason. h per costruire un codice motivo di arresto oppure definire un codice motivo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0b39-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="a0b39-112">Il codice motivo di arresto viene creato da un flag principale, un flag secondario e due flag facoltativi.</span><span class="sxs-lookup"><span data-stu-id="a0b39-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="a0b39-113">Per ulteriori informazioni, vedere [codici motivo dell'arresto del sistema](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a0b39-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0b39-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0b39-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a0b39-115">[Individuazione evento di arresto (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a0b39-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
