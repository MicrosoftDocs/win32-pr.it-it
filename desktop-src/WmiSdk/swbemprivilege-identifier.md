---
description: La proprietà Identifier di un oggetto SWbemPrivilege è un intero WbemPrivilegeEnum che rappresenta il privilegio da impostare o recuperare. Questa proprietà è di sola lettura.
ms.assetid: d370c3ae-6acf-409a-846a-42a74f1a3c02
ms.tgt_platform: multiple
title: Proprietà SWbemPrivilege. Identifier (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Identifier
- ISWbemPrivilege.Identifier
- ISWbemPrivilege.get_Identifier
- ISWbemPrivilege.put_Identifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2906c8f3f49c42471bd05978b35ce33f2cdf11dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968483"
---
# <a name="swbemprivilegeidentifier-property"></a><span data-ttu-id="196ef-104">Proprietà SWbemPrivilege. Identifier</span><span class="sxs-lookup"><span data-stu-id="196ef-104">SWbemPrivilege.Identifier property</span></span>

<span data-ttu-id="196ef-105">La proprietà **Identifier** di un oggetto [**SWbemPrivilege**](swbemprivilege.md) è un intero [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) che rappresenta il privilegio da impostare o recuperare.</span><span class="sxs-lookup"><span data-stu-id="196ef-105">The **Identifier** property of an [**SWbemPrivilege**](swbemprivilege.md) object is an [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) integer that represents the privilege that is being set or retrieved.</span></span> <span data-ttu-id="196ef-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="196ef-106">This property is read-only.</span></span>

<span data-ttu-id="196ef-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="196ef-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="196ef-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="196ef-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="196ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="196ef-109">Syntax</span></span>


```VB
SWbemPrivilege.Identifier As Integer
```



## <a name="property-value"></a><span data-ttu-id="196ef-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="196ef-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="196ef-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="196ef-111">Requirements</span></span>



| <span data-ttu-id="196ef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="196ef-112">Requirement</span></span> | <span data-ttu-id="196ef-113">Valore</span><span class="sxs-lookup"><span data-stu-id="196ef-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="196ef-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="196ef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="196ef-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="196ef-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="196ef-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="196ef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="196ef-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="196ef-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="196ef-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="196ef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="196ef-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="196ef-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="196ef-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="196ef-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="196ef-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="196ef-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="196ef-122">DLL</span><span class="sxs-lookup"><span data-stu-id="196ef-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="196ef-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="196ef-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="196ef-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="196ef-124">CLSID</span></span><br/>                    | <span data-ttu-id="196ef-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="196ef-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="196ef-126">IID</span><span class="sxs-lookup"><span data-stu-id="196ef-126">IID</span></span><br/>                      | <span data-ttu-id="196ef-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="196ef-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="196ef-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="196ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="196ef-129">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="196ef-129">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> <dt>

[<span data-ttu-id="196ef-130">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="196ef-130">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

 




