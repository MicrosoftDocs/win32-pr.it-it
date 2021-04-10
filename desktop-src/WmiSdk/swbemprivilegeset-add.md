---
description: Il metodo Add dell'oggetto SWbemPrivilegeSet aggiunge un oggetto SWbemPrivilege alla raccolta SWbemPrivilegeSet. Se nella raccolta esiste già un privilegio con lo stesso nome, viene sostituito.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049755"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="ce9b6-104">SWbemPrivilegeSet. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="ce9b6-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="ce9b6-105">Il metodo **Add** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="ce9b6-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="ce9b6-106">Se nella raccolta esiste già un privilegio con lo stesso nome, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="ce9b6-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce9b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce9b6-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ce9b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce9b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce9b6-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="ce9b6-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="ce9b6-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-111">Required.</span></span> <span data-ttu-id="ce9b6-112">Una delle costanti WMI del gruppo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="ce9b6-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="ce9b6-113">Queste costanti sono essenzialmente numeri interi che rappresentano privilegi specifici.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="ce9b6-114">Ad esempio, per aggiungere il privilegio che consente di arrestare un sistema di computer, usare la costante **wbemPrivilegeShutdown** .</span><span class="sxs-lookup"><span data-stu-id="ce9b6-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="ce9b6-115">In uno script è necessario usare l'equivalente numerico 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="ce9b6-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="ce9b6-116">Per un elenco completo di queste costanti e delle stringhe dei privilegi associate, vedere [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b6-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce9b6-117">*bIsEnabled* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="ce9b6-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ce9b6-118">Valore booleano che Abilita o Disabilita questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="ce9b6-119">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce9b6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce9b6-120">Return value</span></span>

<span data-ttu-id="ce9b6-121">Se ha esito positivo, il metodo restituisce un oggetto [**SWbemPrivilege**](swbemprivilege.md) che rappresenta il nuovo privilegio.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="ce9b6-122">In caso contrario, viene restituito un oggetto null.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce9b6-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ce9b6-123">Error codes</span></span>

<span data-ttu-id="ce9b6-124">Al termine del metodo **Add** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ce9b6-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ce9b6-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ce9b6-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ce9b6-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ce9b6-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="ce9b6-127">Examples</span></span>

<span data-ttu-id="ce9b6-128">Un esempio di codice che usa questo metodo è descritto nell'argomento [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="ce9b6-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9b6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce9b6-129">Requirements</span></span>



| <span data-ttu-id="ce9b6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce9b6-130">Requirement</span></span> | <span data-ttu-id="ce9b6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ce9b6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9b6-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce9b6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9b6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce9b6-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce9b6-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce9b6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9b6-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce9b6-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce9b6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce9b6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce9b6-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce9b6-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce9b6-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ce9b6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce9b6-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce9b6-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce9b6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ce9b6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce9b6-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce9b6-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce9b6-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="ce9b6-142">CLSID</span></span><br/>                    | <span data-ttu-id="ce9b6-143">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="ce9b6-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="ce9b6-144">IID</span><span class="sxs-lookup"><span data-stu-id="ce9b6-144">IID</span></span><br/>                      | <span data-ttu-id="ce9b6-145">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="ce9b6-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="ce9b6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce9b6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce9b6-147">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="ce9b6-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="ce9b6-148">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="ce9b6-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="ce9b6-149">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="ce9b6-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="ce9b6-150">**SWbemPrivilegeSet.AddAsString**</span><span class="sxs-lookup"><span data-stu-id="ce9b6-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="ce9b6-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="ce9b6-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="ce9b6-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="ce9b6-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="ce9b6-153">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="ce9b6-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




