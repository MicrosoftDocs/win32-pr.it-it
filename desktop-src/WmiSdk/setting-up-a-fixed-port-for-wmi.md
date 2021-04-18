---
description: WMI viene eseguito come parte di un host del servizio condiviso con porte assegnate tramite DCOM per impostazione predefinita. Tuttavia, è possibile configurare il servizio WMI per l'esecuzione come unico processo in un host separato e specificare una porta fissa.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configurazione di una porta fissa per WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318517"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="05287-104">Configurazione di una porta fissa per WMI</span><span class="sxs-lookup"><span data-stu-id="05287-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="05287-105">WMI viene eseguito come parte di un host del servizio condiviso con porte assegnate tramite DCOM per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="05287-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="05287-106">Tuttavia, è possibile configurare il servizio WMI per l'esecuzione come unico processo in un host separato e specificare una porta fissa.</span><span class="sxs-lookup"><span data-stu-id="05287-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="05287-107">La procedura seguente è un'installazione automatica per consentire a WMI di avere una porta fissa.</span><span class="sxs-lookup"><span data-stu-id="05287-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="05287-108">Nella procedura viene utilizzato lo strumento da riga di comando [**WinMgmt**](winmgmt.md) .</span><span class="sxs-lookup"><span data-stu-id="05287-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="05287-109">**Per configurare una porta fissa per WMI**</span><span class="sxs-lookup"><span data-stu-id="05287-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="05287-110">Al prompt dei comandi digitare **winmgmt-standalonehost**</span><span class="sxs-lookup"><span data-stu-id="05287-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="05287-111">Arrestare il servizio WMI digitando il comando **net stop "Strumentazione gestione Windows"** oppure utilizzare il nome breve di **net stop winmgmt**</span><span class="sxs-lookup"><span data-stu-id="05287-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="05287-112">Riavviare nuovamente il servizio WMI in un nuovo host del servizio digitando **net start "Strumentazione gestione Windows"** o **net start WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="05287-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="05287-113">Stabilire un nuovo numero di porta per il servizio WMI digitando **netsh firewall add apertura TCP 24158 WMIFixedPort**</span><span class="sxs-lookup"><span data-stu-id="05287-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="05287-114">Per annullare le modifiche apportate a WMI, digitare **WinMgmt/sharedhost**, quindi arrestare e avviare di nuovo il servizio Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="05287-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="05287-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="05287-115">Examples</span></span>

<span data-ttu-id="05287-116">Per uno script che configura una porta fissa per WMI, vedere il seguente [esempio di codice](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )della raccolta di script.</span><span class="sxs-lookup"><span data-stu-id="05287-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="05287-117">in alternativa, un esempio di codice PowerShell che Abilita o Disabilita le impostazioni della porta WMI, vedere l'esempio [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) nella raccolta TechNet.</span><span class="sxs-lookup"><span data-stu-id="05287-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05287-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05287-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05287-119">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="05287-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="05287-120">Risoluzione dei problemi relativi a connessioni WMI remote</span><span class="sxs-lookup"><span data-stu-id="05287-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="05287-121">Hosting e sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="05287-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



