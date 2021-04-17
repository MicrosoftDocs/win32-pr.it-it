---
description: Il \_ tipo di dati dell'handle SCESVC è un handle opaco fornito dal set di strumenti di configurazione della sicurezza.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525711"
---
# <a name="scesvc_handle"></a><span data-ttu-id="3ba9d-103">\_handle SCESVC</span><span class="sxs-lookup"><span data-stu-id="3ba9d-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="3ba9d-104">Il tipo di dati dell' **\_ handle SCESVC** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3ba9d-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="3ba9d-105">Viene utilizzato dai metodi delle interfacce [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) per passare informazioni tra lo snap-in configurazione di sicurezza e l'estensione dello snap-in.</span><span class="sxs-lookup"><span data-stu-id="3ba9d-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="3ba9d-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ba9d-106">Requirements</span></span>



| <span data-ttu-id="3ba9d-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba9d-107">Requirement</span></span> | <span data-ttu-id="3ba9d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3ba9d-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba9d-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ba9d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba9d-110">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ba9d-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ba9d-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ba9d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba9d-112">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ba9d-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ba9d-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ba9d-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba9d-114"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba9d-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba9d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ba9d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba9d-116">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="3ba9d-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="3ba9d-117">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="3ba9d-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




