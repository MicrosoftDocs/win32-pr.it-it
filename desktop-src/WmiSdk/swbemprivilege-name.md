---
description: La proprietà Name di un oggetto SWbemPrivilege è una stringa che descrive in modo univoco un privilegio.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Proprietà SWbemPrivilege.Name (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233797"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="e6807-103">Proprietà SWbemPrivilege.Name</span><span class="sxs-lookup"><span data-stu-id="e6807-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="e6807-104">La proprietà **Name** di un oggetto [**SWbemPrivilege**](swbemprivilege.md) è una stringa che descrive in modo univoco un privilegio.</span><span class="sxs-lookup"><span data-stu-id="e6807-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="e6807-105">Ad esempio, il privilegio che controlla se un utente può eseguire il metodo Shutdown di un oggetto ha la stringa "SeShutdownPrivilege" nella proprietà **SWbemPrivilege.Name** .</span><span class="sxs-lookup"><span data-stu-id="e6807-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="e6807-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e6807-106">This property is read-only.</span></span>

<span data-ttu-id="e6807-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e6807-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e6807-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e6807-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6807-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6807-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="e6807-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e6807-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e6807-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6807-111">Requirements</span></span>



| <span data-ttu-id="e6807-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6807-112">Requirement</span></span> | <span data-ttu-id="e6807-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e6807-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6807-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6807-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e6807-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6807-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6807-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6807-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e6807-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6807-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6807-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6807-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6807-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6807-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6807-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e6807-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6807-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6807-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6807-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e6807-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6807-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6807-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6807-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="e6807-124">CLSID</span></span><br/>                    | <span data-ttu-id="e6807-125">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="e6807-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="e6807-126">IID</span><span class="sxs-lookup"><span data-stu-id="e6807-126">IID</span></span><br/>                      | <span data-ttu-id="e6807-127">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="e6807-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




