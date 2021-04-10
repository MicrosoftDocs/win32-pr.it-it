---
description: Il metodo Item dell'oggetto SWbemPrivilegeSet restituisce un oggetto SWbemPrivilege dalla raccolta. Il metodo Item è il metodo predefinito di un oggetto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880410"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="02040-104">Metodo SWbemPrivilegeSet. Item</span><span class="sxs-lookup"><span data-stu-id="02040-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="02040-105">Il metodo **Item** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) restituisce un oggetto [**SWbemPrivilege**](swbemprivilege.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="02040-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="02040-106">Il metodo **Item** è il metodo predefinito di un oggetto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="02040-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="02040-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="02040-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02040-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02040-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="02040-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02040-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02040-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="02040-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="02040-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="02040-111">Required.</span></span> <span data-ttu-id="02040-112">Una delle costanti WMI del gruppo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="02040-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="02040-113">Queste costanti sono essenzialmente numeri interi che rappresentano privilegi specifici.</span><span class="sxs-lookup"><span data-stu-id="02040-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="02040-114">Ad esempio, per ottenere il privilegio che consente di arrestare un sistema Windows, usare la costante **wbemPrivilegeShutdown** o l'equivalente numerico 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="02040-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02040-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02040-115">Return value</span></span>

<span data-ttu-id="02040-116">Se l'esito è positivo, viene restituito l'oggetto [**SWbemPrivilege**](swbemprivilege.md) richiesto.</span><span class="sxs-lookup"><span data-stu-id="02040-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02040-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="02040-117">Error codes</span></span>

<span data-ttu-id="02040-118">Al termine del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="02040-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="02040-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="02040-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="02040-120">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="02040-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="02040-121">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="02040-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="02040-122">Il privilegio specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="02040-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="02040-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="02040-123">Examples</span></span>

<span data-ttu-id="02040-124">Nell'esempio di codice VBScript seguente viene usato il metodo **Item**</span><span class="sxs-lookup"><span data-stu-id="02040-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="02040-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02040-125">Requirements</span></span>



| <span data-ttu-id="02040-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="02040-126">Requirement</span></span> | <span data-ttu-id="02040-127">Valore</span><span class="sxs-lookup"><span data-stu-id="02040-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02040-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02040-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02040-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02040-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02040-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02040-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02040-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02040-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02040-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02040-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="02040-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02040-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02040-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="02040-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="02040-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02040-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02040-136">DLL</span><span class="sxs-lookup"><span data-stu-id="02040-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02040-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02040-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02040-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="02040-138">CLSID</span></span><br/>                    | <span data-ttu-id="02040-139">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="02040-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="02040-140">IID</span><span class="sxs-lookup"><span data-stu-id="02040-140">IID</span></span><br/>                      | <span data-ttu-id="02040-141">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="02040-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="02040-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02040-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02040-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="02040-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="02040-144">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="02040-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="02040-145">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="02040-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




