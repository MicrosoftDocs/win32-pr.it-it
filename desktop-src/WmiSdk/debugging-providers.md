---
description: I provider, a meno che non siano provider disaccoppiati in esecuzione all'interno di un'applicazione, vengono caricati in un processo di Wmiprvse.exe e non tramite Svchost.exe con un processo di Winmgmt.exe. Per altre informazioni, vedere Hosting e sicurezza del provider.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Provider di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967130"
---
# <a name="debugging-providers"></a><span data-ttu-id="83e4f-104">Provider di debug</span><span class="sxs-lookup"><span data-stu-id="83e4f-104">Debugging Providers</span></span>

<span data-ttu-id="83e4f-105">I provider, a meno che non siano [*provider disaccoppiati*](gloss-d.md) in esecuzione all'interno di un'applicazione, vengono caricati in un processo di Wmiprvse.exe e non tramite Svchost.exe con un processo di Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="83e4f-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="83e4f-106">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="83e4f-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="83e4f-107">Quando si arresta in corrispondenza di un punto di interruzione, il debugger di Visual Studio blocca l'intero processo host del provider, che in genere è l'host condiviso Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="83e4f-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="83e4f-108">In questo modo si impedisce il funzionamento di tutti gli altri componenti ospitati in tale processo, inclusa l'estensione WMI Esplora server.</span><span class="sxs-lookup"><span data-stu-id="83e4f-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="83e4f-109">Sono bloccate anche le applicazioni client che eseguono chiamate al provider.</span><span class="sxs-lookup"><span data-stu-id="83e4f-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="83e4f-110">I problemi che risultano peggiorano in Windows 2000 e versioni precedenti perché il provider viene caricato nel processo del servizio WMI (Winmgmt.exe).</span><span class="sxs-lookup"><span data-stu-id="83e4f-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="83e4f-111">Se si esegue WMI Esplora server in un'altra istanza, l'IDE di Visual Studio non viene bloccato ed è possibile rilasciare il punto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="83e4f-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="83e4f-112">Si consiglia di eseguire il provider in un processo di hosting distinto durante la fase di sviluppo, in modo che l'arresto in corrispondenza di un punto di interruzione blocchi solo il processo che ospita il provider.</span><span class="sxs-lookup"><span data-stu-id="83e4f-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="83e4f-113">Le altre funzioni di WMI continuano a essere accessibili a WMI Esplora server e a qualsiasi altro script o applicazione basata su WMI.</span><span class="sxs-lookup"><span data-stu-id="83e4f-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="83e4f-114">Inoltre, se il provider si arresta in modo anomalo, non influisce sul funzionamento di altri provider caricati nello stesso processo host.</span><span class="sxs-lookup"><span data-stu-id="83e4f-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="83e4f-115">Per eseguire il caricamento del provider nel proprio processo host, modificare la registrazione del provider per impostare la proprietà [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) su Where il provider `NetworkServiceHost:[MyProvider]` può essere qualsiasi stringa che identifichi in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="83e4f-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="83e4f-116">Usare, ad esempio, il valore **\_ \_ Win32Provider. CLSID** .</span><span class="sxs-lookup"><span data-stu-id="83e4f-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="83e4f-117">Quando il provider è pronto per la spedizione, restituire **\_ \_ Win32Provider. HostingModel** al valore previsto, ad esempio **NetworkServiceHost**.</span><span class="sxs-lookup"><span data-stu-id="83e4f-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="83e4f-118">Se non si esegue il debug del caricamento del provider, è possibile chiamare il [**metodo Load della \_ classe Providers MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) per forzare il caricamento del provider, quindi connettersi al processo di Wmiprvse.exe con la dll caricata ed eseguire il debug in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="83e4f-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83e4f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83e4f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e4f-120">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="83e4f-120">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="83e4f-121">Classi di risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="83e4f-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
