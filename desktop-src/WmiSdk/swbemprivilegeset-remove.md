---
description: Il metodo Remove dell'oggetto SWbemPrivilegeSet Elimina un privilegio dalla raccolta.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882302"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="c3705-103">Metodo SWbemPrivilegeSet. Remove</span><span class="sxs-lookup"><span data-stu-id="c3705-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="c3705-104">Il metodo **Remove** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) Elimina un privilegio dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c3705-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="c3705-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c3705-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3705-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3705-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="c3705-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3705-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3705-108">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="c3705-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="c3705-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3705-109">Required.</span></span> <span data-ttu-id="c3705-110">Si tratta di una delle costanti WMI del gruppo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="c3705-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="c3705-111">Queste costanti sono essenzialmente numeri interi che rappresentano privilegi specifici.</span><span class="sxs-lookup"><span data-stu-id="c3705-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="c3705-112">Ad esempio, per rimuovere il privilegio che consente di arrestare un sistema Windows, usare la costante **wbemPrivilegeShutdown** o l'equivalente numerico di 0x17.</span><span class="sxs-lookup"><span data-stu-id="c3705-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3705-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3705-113">Return value</span></span>

<span data-ttu-id="c3705-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c3705-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3705-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c3705-115">Error codes</span></span>

<span data-ttu-id="c3705-116">Al termine del metodo **Remove** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c3705-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c3705-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c3705-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c3705-118">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c3705-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c3705-119">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="c3705-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c3705-120">Il privilegio specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c3705-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3705-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3705-121">Requirements</span></span>



| <span data-ttu-id="c3705-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3705-122">Requirement</span></span> | <span data-ttu-id="c3705-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c3705-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3705-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3705-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3705-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3705-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3705-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3705-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3705-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3705-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3705-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3705-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3705-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3705-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c3705-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3705-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c3705-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c3705-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3705-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c3705-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="c3705-134">CLSID</span></span><br/>                    | <span data-ttu-id="c3705-135">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="c3705-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="c3705-136">IID</span><span class="sxs-lookup"><span data-stu-id="c3705-136">IID</span></span><br/>                      | <span data-ttu-id="c3705-137">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="c3705-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c3705-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3705-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3705-139">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="c3705-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="c3705-140">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="c3705-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




