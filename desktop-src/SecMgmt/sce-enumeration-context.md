---
description: Il \_ tipo di dati del contesto di enumerazione SCE \_ è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalla \_ funzione informazioni query PFSCE \_ per spostarsi nel database di sicurezza.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343116"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="e1cc5-104">\_contesto di enumerazione SCE \_</span><span class="sxs-lookup"><span data-stu-id="e1cc5-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="e1cc5-105">Il tipo di dati del **\_ \_ contesto di enumerazione SCE** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e1cc5-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="e1cc5-106">Viene usato dalla funzione [**\_ \_ informazioni query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) per spostarsi nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e1cc5-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="e1cc5-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1cc5-107">Requirements</span></span>



| <span data-ttu-id="e1cc5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1cc5-108">Requirement</span></span> | <span data-ttu-id="e1cc5-109">Valore</span><span class="sxs-lookup"><span data-stu-id="e1cc5-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cc5-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1cc5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="e1cc5-111">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1cc5-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e1cc5-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1cc5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="e1cc5-113">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1cc5-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e1cc5-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1cc5-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1cc5-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cc5-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1cc5-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1cc5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cc5-117">**\_informazioni query \_ PFSCE**</span><span class="sxs-lookup"><span data-stu-id="e1cc5-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

