---
title: Come chiamare un metodo WMI
description: Lo scopo principale di WMI è fornire l'accesso alle classi e alle istanze che rappresentano gli oggetti nella rete.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529556"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="af89a-103">Come chiamare un metodo WMI</span><span class="sxs-lookup"><span data-stu-id="af89a-103">How to call a WMI method</span></span>

<span data-ttu-id="af89a-104">Lo scopo principale di WMI è fornire l'accesso alle classi e alle istanze che rappresentano gli oggetti nella rete.</span><span class="sxs-lookup"><span data-stu-id="af89a-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="af89a-105">Queste classi e istanze sono supportate dai provider.</span><span class="sxs-lookup"><span data-stu-id="af89a-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="af89a-106">Ad esempio, tutte le istanze che rappresentano i dispositivi hardware standard nell'azienda, ad esempio [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o la [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), sono supportate dal provider Win32.</span><span class="sxs-lookup"><span data-stu-id="af89a-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="af89a-107">Analogamente, è possibile accedere al registro eventi tramite il provider del registro eventi e il registro di sistema tramite il provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="af89a-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="af89a-108">I metodi implementati da WMI nelle interfacce, ad esempio [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o gli oggetti di scripting come [**SWbemServices**](swbemservices.md), sono principalmente per ottenere e modificare in modo generico i dati forniti da qualsiasi provider.</span><span class="sxs-lookup"><span data-stu-id="af89a-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="af89a-109">Ad esempio, usare [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) per ottenere tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in un subset di computer aziendali.</span><span class="sxs-lookup"><span data-stu-id="af89a-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="af89a-110">È quindi possibile chiamare il metodo del provider Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) in ogni oggetto **\_ processo Win32** .</span><span class="sxs-lookup"><span data-stu-id="af89a-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="af89a-111">Nell'esempio seguente, il metodo [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) viene chiamato come metodo di automazione nell'oggetto Process.</span><span class="sxs-lookup"><span data-stu-id="af89a-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="af89a-112">Un metodo WMI, ad esempio il [**metodo \_ path**](swbemobject-path-.md) definito per [**SWbemObject**](swbemobject.md) , può essere chiamato anche sull'oggetto **Process** .</span><span class="sxs-lookup"><span data-stu-id="af89a-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="af89a-113">Il processo effettivo di utilizzo dei metodi WMI è identico all'utilizzo di qualsiasi altra interfaccia COM o di automazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="af89a-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="af89a-114">Per ulteriori informazioni, vedere [com](../cossdk/component-services-portal.md) e [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="af89a-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="af89a-115">Per ulteriori informazioni sulle interfacce supportate da WMI, vedere [API com per WMI](com-api-for-wmi.md) e [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="af89a-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="af89a-116">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="af89a-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af89a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af89a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af89a-118">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="af89a-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
