---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968485"
---
# <a name="p-wmi"></a><span data-ttu-id="40cba-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="40cba-103">P (WMI)</span></span>

<span data-ttu-id="40cba-104">[A](gloss-a.md) B [C](gloss-c.md) [d](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="40cba-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="40cba-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contatore delle prestazioni**</span><span class="sxs-lookup"><span data-stu-id="40cba-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-106">Proprietà in una classe di prestazioni derivata da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) che archivia i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="40cba-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="40cba-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**oggetto prestazioni**</span><span class="sxs-lookup"><span data-stu-id="40cba-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-108">Oggetto in una libreria di prestazioni che archivia i dati nei contatori.</span><span class="sxs-lookup"><span data-stu-id="40cba-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="40cba-109">Questi oggetti sono visibili nell'utilità [*Monitor di sistema*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="40cba-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="40cba-110">Gli esempi sono oggetti cache e disco logico.</span><span class="sxs-lookup"><span data-stu-id="40cba-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="40cba-111">Quando viene trasferito in WMI dal processo [*ADAP*](gloss-a.md) , ogni oggetto diventa due classi di prestazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="40cba-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="40cba-112">Una classe che contiene dati non elaborati deriva da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="40cba-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="40cba-113">L'altra classe deriva da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e contiene gli stessi dati visibili in Monitor di sistema calcolato dal provider del contatore cotto.</span><span class="sxs-lookup"><span data-stu-id="40cba-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="40cba-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumer permanente**</span><span class="sxs-lookup"><span data-stu-id="40cba-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-115">Un [*consumer di eventi*](gloss-e.md) la cui registrazione dura finché non viene annullata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="40cba-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="40cba-116">Vedere anche [*consumer temporaneo*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="40cba-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="40cba-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumer fisico**</span><span class="sxs-lookup"><span data-stu-id="40cba-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-118">Oggetto COM implementato da un [*provider di consumer di eventi*](gloss-e.md) che include un [*sink*](gloss-s.md) per la ricezione delle notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="40cba-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="40cba-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="40cba-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-120">Coppia nome/valore che descrive un'unità di dati per una classe.</span><span class="sxs-lookup"><span data-stu-id="40cba-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="40cba-121">I valori delle proprietà devono avere un tipo di dati [*Managed Object Format (MOF)*](gloss-m.md) valido.</span><span class="sxs-lookup"><span data-stu-id="40cba-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="40cba-122">Vedere anche [*Proprietà Reference*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="40cba-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="40cba-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**provider di proprietà**</span><span class="sxs-lookup"><span data-stu-id="40cba-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-124">Server COM che supporta il recupero e la modifica delle proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="40cba-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="40cba-125">I provider di proprietà implementano le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .</span><span class="sxs-lookup"><span data-stu-id="40cba-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="40cba-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span><span class="sxs-lookup"><span data-stu-id="40cba-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-127">Server COM che comunica con oggetti gestiti per accedere ai dati e alle notifiche degli eventi, ad esempio il registro di sistema o un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="40cba-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="40cba-128">I provider inviano questi dati al [*CIM Object Manager*](gloss-c.md) per l'integrazione e l'interpretazione.</span><span class="sxs-lookup"><span data-stu-id="40cba-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="40cba-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**Metodo del provider**</span><span class="sxs-lookup"><span data-stu-id="40cba-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="40cba-130">Metodo implementato da un *provider* WMI.</span><span class="sxs-lookup"><span data-stu-id="40cba-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
