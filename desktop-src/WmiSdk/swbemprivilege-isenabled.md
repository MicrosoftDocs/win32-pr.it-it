---
description: La proprietà IsEnabled di un oggetto SWbemPrivilege è un valore booleano che viene usato per abilitare o disabilitare questo privilegio. Per ulteriori informazioni sulle conseguenze dell'abilitazione di privilegi specifici, vedere esecuzione con privilegi speciali.
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: Proprietà SWbemPrivilege. IsEnabled (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309797"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="148cb-104">Proprietà SWbemPrivilege. IsEnabled</span><span class="sxs-lookup"><span data-stu-id="148cb-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="148cb-105">La proprietà **IsEnabled** di un oggetto [**SWbemPrivilege**](swbemprivilege.md) è un valore booleano che viene usato per abilitare o disabilitare questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="148cb-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="148cb-106">Per ulteriori informazioni sulle conseguenze dell'abilitazione di privilegi specifici, vedere [**esecuzione con privilegi speciali**](swbemsecurity-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="148cb-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="148cb-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="148cb-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="148cb-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="148cb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="148cb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="148cb-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="148cb-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="148cb-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="148cb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="148cb-111">Requirements</span></span>



| <span data-ttu-id="148cb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="148cb-112">Requirement</span></span> | <span data-ttu-id="148cb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="148cb-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="148cb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="148cb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="148cb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="148cb-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="148cb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="148cb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="148cb-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="148cb-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="148cb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="148cb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="148cb-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="148cb-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="148cb-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="148cb-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="148cb-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="148cb-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="148cb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="148cb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148cb-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="148cb-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="148cb-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="148cb-124">CLSID</span></span><br/>                    | <span data-ttu-id="148cb-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="148cb-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="148cb-126">IID</span><span class="sxs-lookup"><span data-stu-id="148cb-126">IID</span></span><br/>                      | <span data-ttu-id="148cb-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="148cb-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




