---
description: Il provider WDM (Windows Driver Model) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Provider WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753711"
---
# <a name="wdm-provider"></a><span data-ttu-id="5c0f8-103">Provider WDM</span><span class="sxs-lookup"><span data-stu-id="5c0f8-103">WDM Provider</span></span>

<span data-ttu-id="5c0f8-104">Il provider WDM (Windows Driver Model) concede l'accesso alle classi, alle istanze, ai metodi e agli eventi dei driver hardware conformi al modello WDM.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="5c0f8-105">Le classi per i driver hardware si trovano nello " \\ spazio dei nomi WMI radice".</span><span class="sxs-lookup"><span data-stu-id="5c0f8-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="5c0f8-106">Le classi WDM sono definite principalmente in WMI. mof.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="5c0f8-107">WDM è un'interfaccia del sistema operativo tramite la quale i componenti hardware forniscono informazioni e notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="5c0f8-108">Il provider WDM è una classe, un'istanza, un evento e un provider di metodi che consente alle applicazioni di gestione di accedere a dati ed eventi da driver di dispositivo abilitati per WMI per WDM.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="5c0f8-109">Le classi create dal provider WDM per rappresentare i dati dei driver di dispositivo risiedono solo nello \\ spazio dei nomi "WMI radice".</span><span class="sxs-lookup"><span data-stu-id="5c0f8-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="5c0f8-110">Questo spazio dei nomi deve esistere già prima che il provider WDM elabori i driver WDM installati.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="5c0f8-111">Il provider WDM registra le informazioni sulle operazioni WDM nel file WmiProv. log.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="5c0f8-112">Per ulteriori informazioni, vedere [file di log WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="5c0f8-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="5c0f8-113">Come classe, istanza, metodo e provider di eventi, il provider WDM implementa l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, oltre ai metodi [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c0f8-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="5c0f8-114">**CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="5c0f8-115">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="5c0f8-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="5c0f8-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="5c0f8-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="5c0f8-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="5c0f8-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="5c0f8-121">Il provider WDM supporta l'evento estrinseco [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) , che informa WMI sugli eventi di driver basati su WDM.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="5c0f8-122">È possibile registrare i consumer di eventi per gli eventi **WmiEvent** come per qualsiasi altro evento.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="5c0f8-123">Per ulteriori informazioni, vedere [ricezione di un evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="5c0f8-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="5c0f8-124">Quando si avvia un driver non viene generato alcun evento di creazione della classe.</span><span class="sxs-lookup"><span data-stu-id="5c0f8-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="5c0f8-125">Il provider WDM supporta la classe seguente:</span><span class="sxs-lookup"><span data-stu-id="5c0f8-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="5c0f8-126">**WMIBinaryMofResource**</span><span class="sxs-lookup"><span data-stu-id="5c0f8-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="5c0f8-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c0f8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c0f8-128">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="5c0f8-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="5c0f8-129">Accesso ai dati dai driver di dispositivo</span><span class="sxs-lookup"><span data-stu-id="5c0f8-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
