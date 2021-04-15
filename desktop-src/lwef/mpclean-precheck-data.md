---
title: Struttura MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Dati di notifica passati per pulire la funzione di callback di verifica.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- Struttura MPCLEAN_PRECHECK_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCLEAN_PRECHECK_DATA
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476115"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="a1c87-105">\_Struttura dei dati di PREVERIFICA MPCLEAN \_</span><span class="sxs-lookup"><span data-stu-id="a1c87-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="a1c87-106">Dati di notifica passati per pulire la funzione di callback di verifica.</span><span class="sxs-lookup"><span data-stu-id="a1c87-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c87-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1c87-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="a1c87-108">Members</span><span class="sxs-lookup"><span data-stu-id="a1c87-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1c87-109">**BlockedResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="a1c87-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a1c87-110">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="a1c87-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="a1c87-111">Informazioni sulle risorse per la risorsa bloccata.</span><span class="sxs-lookup"><span data-stu-id="a1c87-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="a1c87-112">Ad esempio, quando lo stato di avanzamento è **MPNOTIFY la \_ Preverifica della \_ risorsa \_ bloccata**.</span><span class="sxs-lookup"><span data-stu-id="a1c87-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="a1c87-113">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="a1c87-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1c87-114">**\_informazioni PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="a1c87-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="a1c87-115">Tipo: **BlockingResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="a1c87-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="a1c87-116">Informazioni sulle risorse che stanno bloccando.</span><span class="sxs-lookup"><span data-stu-id="a1c87-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="a1c87-117">Ad esempio, quando lo stato di avanzamento è **MPNOTIFY la \_ Preverifica della \_ risorsa \_ bloccata**.</span><span class="sxs-lookup"><span data-stu-id="a1c87-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="a1c87-118">Vedere [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="a1c87-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1c87-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1c87-119">Requirements</span></span>



| <span data-ttu-id="a1c87-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1c87-120">Requirement</span></span> | <span data-ttu-id="a1c87-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a1c87-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c87-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1c87-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c87-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a1c87-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a1c87-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1c87-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c87-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a1c87-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1c87-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1c87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1c87-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c87-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c87-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1c87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c87-129">**\_informazioni MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="a1c87-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





