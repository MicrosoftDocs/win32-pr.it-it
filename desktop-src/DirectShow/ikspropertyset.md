---
description: L'interfaccia IKsPropertySet è stata originariamente progettata come un modo efficiente per impostare e recuperare le proprietà dei dispositivi nei driver WDM, usando KSProxy per tradurre le chiamate al metodo COM in modalità utente nei set di proprietà in modalità kernel usati dai driver della classe di streaming WDM. Questa interfaccia viene ora utilizzata anche per passare le informazioni esclusivamente tra i componenti software. In alcuni casi, i componenti software devono implementare questa interfaccia, altrimenti l'interfaccia IKsControl (documentata in DirectShow DDK). Se, ad esempio, si scrive un decodificatore MPEG-2 software da utilizzare con lo strumento di spostamento DVD, è necessario implementare una di queste interfacce e supportare anche i set di proprietà correlati a DVD che lo strumento di spostamento invierà al decodificatore. I pin possono supportare una di queste interfacce per consentire ad altri pin o filtri di impostare o recuperare le proprietà. Si noti che nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia IKsControl, documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interfaccia IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480772"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="d5ab2-109">Interfaccia IKsPropertySet</span><span class="sxs-lookup"><span data-stu-id="d5ab2-109">IKsPropertySet interface</span></span>

<span data-ttu-id="d5ab2-110">L' `IKsPropertySet` interfaccia è stata originariamente progettata come un modo efficiente per impostare e recuperare le proprietà dei dispositivi nei driver WDM, usando ksproxy per tradurre le chiamate al metodo com in modalità utente nei set di proprietà in modalità kernel usati dai driver della classe di streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="d5ab2-111">Questa interfaccia viene ora utilizzata anche per passare le informazioni esclusivamente tra i componenti software.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="d5ab2-112">In alcuni casi, i componenti software devono implementare questa interfaccia, altrimenti l'interfaccia **IKsControl** (documentata in DirectShow DDK).</span><span class="sxs-lookup"><span data-stu-id="d5ab2-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="d5ab2-113">Se, ad esempio, si scrive un decodificatore MPEG-2 software da utilizzare con lo [strumento di spostamento DVD](dvd-navigator-filter.md), è necessario implementare una di queste interfacce e supportare anche i set di proprietà correlati a DVD che lo strumento di spostamento invierà al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="d5ab2-114">I pin possono supportare una di queste interfacce per consentire ad altri pin o filtri di impostare o recuperare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="d5ab2-115">Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="d5ab2-116">Le due interfacce non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="d5ab2-117">L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="d5ab2-118">Membri</span><span class="sxs-lookup"><span data-stu-id="d5ab2-118">Members</span></span>

<span data-ttu-id="d5ab2-119">L'interfaccia **IKsPropertySet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5ab2-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5ab2-120">**IKsPropertySet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5ab2-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="d5ab2-121">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5ab2-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5ab2-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5ab2-122">Methods</span></span>

<span data-ttu-id="d5ab2-123">L'interfaccia **IKsPropertySet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="d5ab2-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="d5ab2-124">Method</span></span>                                                  | <span data-ttu-id="d5ab2-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5ab2-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5ab2-126">**Ottieni**</span><span class="sxs-lookup"><span data-stu-id="d5ab2-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="d5ab2-127">Recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="d5ab2-128">**QuerySupported**</span><span class="sxs-lookup"><span data-stu-id="d5ab2-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="d5ab2-129">Determina se un oggetto supporta un set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="d5ab2-130">**Set**</span><span class="sxs-lookup"><span data-stu-id="d5ab2-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="d5ab2-131">Imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="d5ab2-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5ab2-132">Remarks</span></span>

<span data-ttu-id="d5ab2-133">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="d5ab2-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ab2-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5ab2-134">Requirements</span></span>



| <span data-ttu-id="d5ab2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ab2-135">Requirement</span></span> | <span data-ttu-id="d5ab2-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d5ab2-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ab2-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5ab2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ab2-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5ab2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5ab2-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5ab2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ab2-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5ab2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5ab2-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5ab2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ab2-142"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ab2-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="d5ab2-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5ab2-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5ab2-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5ab2-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ab2-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5ab2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ab2-146">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="d5ab2-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
