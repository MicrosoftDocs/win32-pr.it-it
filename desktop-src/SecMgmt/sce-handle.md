---
description: Il \_ tipo di dati dell'handle SCE è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalle \_ \_ funzioni info query PFSCE e PFSCE \_ set \_ Info Support per passare le informazioni tra l'allegato e il database di sicurezza.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128774"
---
# <a name="sce_handle"></a><span data-ttu-id="07145-104">\_handle SCE</span><span class="sxs-lookup"><span data-stu-id="07145-104">SCE\_HANDLE</span></span>

<span data-ttu-id="07145-105">Il tipo di dati dell' **\_ handle SCE** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="07145-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="07145-106">Viene usato dalle funzioni [**\_ \_ info query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support per passare le informazioni tra l'allegato e il database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="07145-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="07145-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07145-107">Requirements</span></span>



| <span data-ttu-id="07145-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="07145-108">Requirement</span></span> | <span data-ttu-id="07145-109">Valore</span><span class="sxs-lookup"><span data-stu-id="07145-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07145-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07145-110">Minimum supported client</span></span><br/> | <span data-ttu-id="07145-111">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="07145-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="07145-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07145-112">Minimum supported server</span></span><br/> | <span data-ttu-id="07145-113">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07145-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07145-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07145-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="07145-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="07145-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07145-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07145-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07145-117">**\_informazioni query \_ PFSCE**</span><span class="sxs-lookup"><span data-stu-id="07145-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="07145-118">**\_informazioni sul set di PFSCE \_**</span><span class="sxs-lookup"><span data-stu-id="07145-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

