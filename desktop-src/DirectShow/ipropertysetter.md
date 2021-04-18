---
description: "L'interfaccia IPropertySetter imposta le proprietà per un effetto o una transizione in servizi di modifica DirectShow (DES). Per usare questa interfaccia, creare un'istanza di un oggetto Setter di proprietà (CLSID \\_ PropertySetter) e associarla a un effetto o una transizione chiamando il metodo IAMTimelineObj:: SetPropertySetter. Per altre informazioni, vedere uso degli effetti e delle transizioni. in genere, un'applicazione deve chiamare solo il metodo IPropertySetter:: ClearProps per cancellare le proprietà esistenti e il metodo IPropertySetter:: AddProp per aggiungere nuove proprietà. Gli altri metodi di questa interfaccia vengono chiamati da altri componenti DES."
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaccia IPropertySetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329753"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="6e8d0-105">Interfaccia IPropertySetter</span><span class="sxs-lookup"><span data-stu-id="6e8d0-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="6e8d0-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-106">\[Deprecated.</span></span> <span data-ttu-id="6e8d0-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6e8d0-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6e8d0-108">L' `IPropertySetter` interfaccia imposta le proprietà per un effetto o una transizione in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="6e8d0-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="6e8d0-109">Per usare questa interfaccia, creare un'istanza di un oggetto Setter di proprietà (CLSID \_ PropertySetter) e associarla a un effetto o una transizione chiamando il metodo [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8d0-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="6e8d0-110">Per ulteriori informazioni, vedere [utilizzo di effetti e transizioni](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="6e8d0-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="6e8d0-111">In genere, un'applicazione deve chiamare solo il metodo [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) per cancellare le proprietà esistenti e il metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) per aggiungere nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="6e8d0-112">Gli altri metodi di questa interfaccia vengono chiamati da altri componenti DES.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="6e8d0-113">Membri</span><span class="sxs-lookup"><span data-stu-id="6e8d0-113">Members</span></span>

<span data-ttu-id="6e8d0-114">L'interfaccia **IPropertySetter** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6e8d0-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6e8d0-115">**IPropertySetter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6e8d0-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="6e8d0-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e8d0-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6e8d0-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e8d0-117">Methods</span></span>

<span data-ttu-id="6e8d0-118">L'interfaccia **IPropertySetter** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="6e8d0-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="6e8d0-119">Method</span></span>                                               | <span data-ttu-id="6e8d0-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8d0-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e8d0-121">**AddProp**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="6e8d0-122">Aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="6e8d0-123">**ClearProps**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="6e8d0-124">Cancella tutti i dati della proprietà dal setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="6e8d0-125">**CloneProps**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="6e8d0-126">Clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="6e8d0-127">**FreeProps**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="6e8d0-128">Libera le risorse allocate dal metodo [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8d0-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="6e8d0-129">**GetProps**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="6e8d0-130">Recupera le proprietà impostate per questo oggetto con i valori corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="6e8d0-131">**LoadFromBlob**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="6e8d0-132">Carica i dati della proprietà da un formato di persistenza.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="6e8d0-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="6e8d0-134">Carica i dati delle proprietà espressi in Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="6e8d0-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="6e8d0-135">**PrintXML**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="6e8d0-136">Converte i dati della proprietà in una stringa XML.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="6e8d0-137">**SaveToBlob**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="6e8d0-138">Salva i dati della proprietà in un formato di persistenza.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="6e8d0-139">**SetProps**</span><span class="sxs-lookup"><span data-stu-id="6e8d0-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="6e8d0-140">Imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="6e8d0-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e8d0-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e8d0-142">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6e8d0-143">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6e8d0-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6e8d0-144">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6e8d0-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e8d0-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e8d0-145">Requirements</span></span>



| <span data-ttu-id="6e8d0-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e8d0-146">Requirement</span></span> | <span data-ttu-id="6e8d0-147">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8d0-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8d0-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e8d0-148">Header</span></span><br/>  | <dl> <span data-ttu-id="6e8d0-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e8d0-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6e8d0-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e8d0-150">Library</span></span><br/> | <dl> <span data-ttu-id="6e8d0-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e8d0-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
