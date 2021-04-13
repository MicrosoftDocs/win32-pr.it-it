---
description: È possibile utilizzare le proprietà dell'oggetto SWbemMethod per controllare la definizione di un singolo metodo di un oggetto WMI. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Oggetto SWbemMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528488"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="834b5-104">Oggetto SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="834b5-104">SWbemMethod object</span></span>

<span data-ttu-id="834b5-105">È possibile utilizzare le proprietà dell'oggetto **SWbemMethod** per controllare la definizione di un singolo metodo di un oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="834b5-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="834b5-106">Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="834b5-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="834b5-107">Questo oggetto può essere utilizzato per controllare le definizioni dei metodi.</span><span class="sxs-lookup"><span data-stu-id="834b5-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="834b5-108">Per richiamare i metodi, è consigliabile usare l'accesso diretto (vedere [modifica delle informazioni di classe e istanza](manipulating-class-and-instance-information.md)) in un oggetto [**SWbemObject**](swbemobject.md) (che è il meccanismo consigliato) o la chiamata [**cMethodSWbemServices.Exe**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="834b5-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="834b5-109">In questa versione dell'API, l'accesso in scrittura alle informazioni sul metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="834b5-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="834b5-110">Se si desidera definire metodi o modificare definizioni di metodo esistenti, è possibile definire le modifiche al metodo in un file MOF e inviare le modifiche utilizzando il [compilatore MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="834b5-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="834b5-111">In alternativa, usare l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="834b5-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="834b5-112">Membri</span><span class="sxs-lookup"><span data-stu-id="834b5-112">Members</span></span>

<span data-ttu-id="834b5-113">L'oggetto **SWbemMethod** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="834b5-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="834b5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="834b5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="834b5-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="834b5-115">Properties</span></span>

<span data-ttu-id="834b5-116">L'oggetto **SWbemMethod** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="834b5-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="834b5-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="834b5-117">Property</span></span>                                                      | <span data-ttu-id="834b5-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="834b5-118">Access type</span></span>          | <span data-ttu-id="834b5-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="834b5-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="834b5-120">**InParameters**</span><span class="sxs-lookup"><span data-stu-id="834b5-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="834b5-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="834b5-121">Read-only</span></span><br/> | <span data-ttu-id="834b5-122">Oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri di input per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="834b5-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="834b5-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="834b5-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="834b5-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="834b5-124">Read-only</span></span><br/> | <span data-ttu-id="834b5-125">Nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="834b5-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="834b5-126">**Origine**</span><span class="sxs-lookup"><span data-stu-id="834b5-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="834b5-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="834b5-127">Read-only</span></span><br/> | <span data-ttu-id="834b5-128">Classe di origine del metodo.</span><span class="sxs-lookup"><span data-stu-id="834b5-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="834b5-129">**OutParameters**</span><span class="sxs-lookup"><span data-stu-id="834b5-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="834b5-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="834b5-130">Read-only</span></span><br/> | <span data-ttu-id="834b5-131">Oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="834b5-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="834b5-132">**Qualificatori\_**</span><span class="sxs-lookup"><span data-stu-id="834b5-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="834b5-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="834b5-133">Read-only</span></span><br/> | <span data-ttu-id="834b5-134">Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che contiene i qualificatori per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="834b5-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="834b5-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="834b5-135">Requirements</span></span>



| <span data-ttu-id="834b5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="834b5-136">Requirement</span></span> | <span data-ttu-id="834b5-137">Valore</span><span class="sxs-lookup"><span data-stu-id="834b5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="834b5-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="834b5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="834b5-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="834b5-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="834b5-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="834b5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="834b5-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="834b5-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="834b5-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="834b5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="834b5-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="834b5-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="834b5-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="834b5-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="834b5-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="834b5-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="834b5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="834b5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="834b5-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834b5-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="834b5-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="834b5-148">CLSID</span></span><br/>                    | <span data-ttu-id="834b5-149">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="834b5-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="834b5-150">IID</span><span class="sxs-lookup"><span data-stu-id="834b5-150">IID</span></span><br/>                      | <span data-ttu-id="834b5-151">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="834b5-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="834b5-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="834b5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834b5-153">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="834b5-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




