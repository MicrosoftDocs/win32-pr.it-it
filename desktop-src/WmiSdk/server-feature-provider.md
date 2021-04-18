---
description: A partire da Windows Server 2008, il provider di funzionalità server fornisce informazioni sulle funzionalità server installate nel server. Questa classe consente agli amministratori di inventariare e gestire i ruoli e le funzionalità del server.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Provider di funzionalità server
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313176"
---
# <a name="server-feature-provider"></a><span data-ttu-id="baec7-104">Provider di funzionalità server</span><span class="sxs-lookup"><span data-stu-id="baec7-104">Server Feature Provider</span></span>

<span data-ttu-id="baec7-105">A partire da Windows Server 2008, il provider di funzionalità server fornisce informazioni sulle funzionalità server installate nel server.</span><span class="sxs-lookup"><span data-stu-id="baec7-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="baec7-106">Questa classe consente agli amministratori di inventariare e gestire i ruoli e le funzionalità del server.</span><span class="sxs-lookup"><span data-stu-id="baec7-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="baec7-107">Un ruolo del server è definito come un gruppo di componenti che forniscono funzioni per un'area specifica di funzionalità, ad esempio la stampa, i file, il controllo del dominio e così via.</span><span class="sxs-lookup"><span data-stu-id="baec7-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="baec7-108">I ruoli del server tipici sono file server, server di posta elettronica, server DNS, controller di dominio, server applicazioni e così via.</span><span class="sxs-lookup"><span data-stu-id="baec7-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="baec7-109">Se un'organizzazione non esegue un software di gestione che segnala i ruoli del server, ad esempio Microsoft Operations Manager con i Management Pack installati, è possibile ottenere tali informazioni eseguendo una query sulla classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) .</span><span class="sxs-lookup"><span data-stu-id="baec7-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="baec7-110">Il ruolo del server e le informazioni sulle funzionalità dei computer remoti sono disponibili tramite le normali connessioni remote WMI o tramite il servizio Gestione remota Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="baec7-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="baec7-111">Per ulteriori informazioni sulle connessioni DCOM remote WMI, vedere [la pagina relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="baec7-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="baec7-112">Per ulteriori informazioni sulle connessioni che utilizzano il protocollo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , vedere [gestione remota Windows](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="baec7-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="baec7-113">Il provider di funzionalità Server supporta le classi WMI seguenti:</span><span class="sxs-lookup"><span data-stu-id="baec7-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="baec7-114">**\_ServerFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="baec7-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="baec7-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="baec7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baec7-116">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="baec7-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
