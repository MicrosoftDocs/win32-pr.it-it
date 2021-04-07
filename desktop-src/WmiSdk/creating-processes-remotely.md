---
description: È possibile utilizzare Win32 \_ Process. create per eseguire uno script o un'applicazione in un computer remoto. Tuttavia, per motivi di sicurezza, il processo non può essere interattivo. Quando Win32 \_ Process. Create viene chiamato sul computer locale, il processo può essere interattivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Creazione di processi in modalità remota tramite WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758747"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="868e3-105">Creazione di processi in modalità remota tramite WMI</span><span class="sxs-lookup"><span data-stu-id="868e3-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="868e3-106">È possibile utilizzare [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) per eseguire uno script o un'applicazione in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="868e3-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="868e3-107">Tuttavia, per motivi di sicurezza, il processo non può essere interattivo.</span><span class="sxs-lookup"><span data-stu-id="868e3-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="868e3-108">Quando **Win32 \_ Process. Create** viene chiamato sul computer locale, il processo può essere interattivo.</span><span class="sxs-lookup"><span data-stu-id="868e3-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="868e3-109">In questo argomento viene descritta la procedura generale per la creazione di un processo remoto con WMI.</span><span class="sxs-lookup"><span data-stu-id="868e3-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="868e3-110">Se si sta semplicemente cercando di eseguire uno script in un sistema remoto, vedere [connessione a WMI in modalità remota a partire da Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)o [connessione a WMI in un computer remoto tramite Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="868e3-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="868e3-111">Per informazioni più generali sulla comunicazione remota con PowerShell, vedere [esecuzione di comandi remoti](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="868e3-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="868e3-112">Il processo remoto non dispone di alcuna interfaccia utente, ma è elencato in **Gestione attività**.</span><span class="sxs-lookup"><span data-stu-id="868e3-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="868e3-113">Un processo creato localmente può essere eseguito con qualsiasi account se l'account dispone dell'autorizzazione **Execute Method** per lo \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="868e3-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="868e3-114">Un processo creato in modalità remota può essere eseguito con qualsiasi account se l'account dispone delle autorizzazioni **Esegui metodo** e **Abilita remoto** per \\ CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="868e3-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="868e3-115">Le autorizzazioni **Execute Method** e **Remote Enable** sono impostate nel controllo WMI nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="868e3-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="868e3-116">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="868e3-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="868e3-117">È possibile utilizzare [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) per creare un processo interattivo in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="868e3-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="868e3-118">Ma i processi avviati da **Win32 \_ ScheduledJob. Create** vengono eseguiti con l'account LocalSystem che può conferire un privilegio troppo elevato.</span><span class="sxs-lookup"><span data-stu-id="868e3-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="868e3-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="868e3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="868e3-120">Protezione di una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="868e3-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="868e3-121">Connessione a un terzo computer-delega</span><span class="sxs-lookup"><span data-stu-id="868e3-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
