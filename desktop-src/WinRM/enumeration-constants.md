---
title: Costanti di enumerazione (WSManDisp. h)
description: L'enumerazione contiene costanti, elencate nell'elenco seguente, utilizzate nel parametro flags dalle chiamate a Session. enumerate e IWSManSession.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400428"
---
# <a name="enumeration-constants"></a><span data-ttu-id="2bdf0-103">Costanti di enumerazione</span><span class="sxs-lookup"><span data-stu-id="2bdf0-103">Enumeration Constants</span></span>

<span data-ttu-id="2bdf0-104">L'enumerazione **\_ \_ WSManEnumFlags** contiene costanti, elencate nell'elenco seguente, utilizzate nel parametro *Flags* dalle chiamate a [**Session. enumerate**](session-enumerate.md) e [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="2bdf0-105">Tenere presente che **WSManFlagReturnObject** e **WSManFlagHierarchyDeep** sono i valori predefiniti se il parametro *Flags* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="2bdf0-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-107">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-108">I batch contengono le istanze XML richieste.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="2bdf0-109">Si tratta del valore predefinito per il parametro del flag.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="2bdf0-110">Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-113">Questo flag controlla il modo in cui il parametro *Filter* nella chiamata a [**Session. enumerate**](session-enumerate.md) viene interpretato da WinRM.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="2bdf0-114">Il formato del filtro può essere un frammento XML o una stringa di testo normale.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="2bdf0-115">Il formato è determinato dal [*dialetto del filtro*](windows-remote-management-glossary.md) [*utilizzato nella*](windows-remote-management-glossary.md) chiamata a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), che è specifico dell'operazione eseguita.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="2bdf0-116">Se il parametro *dialect* non è specificato, WinRM tenta di determinare il dialetto in base al primo carattere del filtro.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="2bdf0-117">Se il primo carattere è <, ma il filtro non è effettivamente un frammento XML, è necessario impostare questo flag.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="2bdf0-118">Un filtro nel formato seguente, ad esempio, richiede l'impostazione di **WSManFlagNonXmlText** in modo che il filtro venga interpretato correttamente:</span><span class="sxs-lookup"><span data-stu-id="2bdf0-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="2bdf0-119">Se il filtro è un frammento XML, questo flag non è necessario perché il frammento inizia con <, che WinRM interpreta correttamente come XML.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="2bdf0-120">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="2bdf0-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="2bdf0-121">Se il filtro è in testo normale che non inizia con <, questo flag non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="2bdf0-122">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="2bdf0-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="2bdf0-123">Il metodo di scripting associato è [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) e il metodo C++ è [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-126">I batch contengono riferimenti a endpoint (EPRs) per le istanze XML corrispondenti, ma non le istanze effettive.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="2bdf0-127">Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-130">I batch contengono sia le istanze XML richieste che i EPRs corrispondenti contenuti in un elemento [*WSMan: Items*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="2bdf0-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="2bdf0-131">Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-133">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-134">Le istanze delle classi derivate sono incluse e sono rappresentate in base agli schemi effettivi.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="2bdf0-135">Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-138">Le istanze delle classi derivate sono escluse.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-138">Derived class instances are excluded.</span></span> <span data-ttu-id="2bdf0-139">Vengono visualizzate solo le istanze del tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="2bdf0-140">Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2bdf0-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="2bdf0-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdf0-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="2bdf0-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="2bdf0-143">Le istanze delle classi derivate sono incluse e sono rappresentate in base allo schema della classe di base.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="2bdf0-144">Le proprietà definite nella classe derivata non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="2bdf0-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="2bdf0-145">Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="2bdf0-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bdf0-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bdf0-146">Requirements</span></span>



| <span data-ttu-id="2bdf0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bdf0-147">Requirement</span></span> | <span data-ttu-id="2bdf0-148">Valore</span><span class="sxs-lookup"><span data-stu-id="2bdf0-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdf0-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bdf0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdf0-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bdf0-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2bdf0-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bdf0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdf0-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bdf0-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2bdf0-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bdf0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bdf0-154"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bdf0-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bdf0-155">IDL</span><span class="sxs-lookup"><span data-stu-id="2bdf0-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bdf0-156"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bdf0-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bdf0-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bdf0-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdf0-158">Costanti ed enumerazioni WinRM</span><span class="sxs-lookup"><span data-stu-id="2bdf0-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="2bdf0-159">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="2bdf0-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="2bdf0-160">Esecuzione di query per istanze specifiche di una risorsa</span><span class="sxs-lookup"><span data-stu-id="2bdf0-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





