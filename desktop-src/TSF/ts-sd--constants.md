---
title: Costanti TS_SD_ (Textstor. h)
description: Le \_ costanti SD \_ \ ts descrivono gli Stati dei documenti dinamici usati da un'applicazione in fase di esecuzione.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301344"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="0285e-103">\_Costanti SD \_ \* TS</span><span class="sxs-lookup"><span data-stu-id="0285e-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="0285e-104">Le \_ costanti SD TS \_ \* descrivono gli Stati dei documenti dinamici usati da un'applicazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0285e-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="0285e-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="0285e-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="0285e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0285e-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="0285e-107"><dt>**Servizi terminal \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0285e-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="0285e-108">Il documento è di sola lettura e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="0285e-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="0285e-109"><dt>**Servizi terminal \_ \_Caricamento SD**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0285e-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="0285e-110">Il documento viene caricato e potrebbe essere incompleto.</span><span class="sxs-lookup"><span data-stu-id="0285e-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="0285e-111"><dt>**Servizi terminal \_ SD \_ MASKALL**</dt> <dt>( \_ \_ \| \_ \_ caricamento SD TS SD ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="0285e-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="0285e-112">Il documento è di sola lettura e viene caricato.</span><span class="sxs-lookup"><span data-stu-id="0285e-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="0285e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0285e-113">Remarks</span></span>

<span data-ttu-id="0285e-114">Il membro **dwDynamicFlags** della struttura [di \_ stato TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) usa queste costanti.</span><span class="sxs-lookup"><span data-stu-id="0285e-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="0285e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0285e-115">Requirements</span></span>



| <span data-ttu-id="0285e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0285e-116">Requirement</span></span> | <span data-ttu-id="0285e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0285e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0285e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0285e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0285e-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0285e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0285e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0285e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0285e-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0285e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0285e-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0285e-122">Redistributable</span></span><br/>          | <span data-ttu-id="0285e-123">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0285e-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="0285e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0285e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0285e-125"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="0285e-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="0285e-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0285e-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0285e-127"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0285e-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0285e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0285e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0285e-129">stato di Servizi terminal \_</span><span class="sxs-lookup"><span data-stu-id="0285e-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="0285e-130">\_Costanti SD \_ \* TF</span><span class="sxs-lookup"><span data-stu-id="0285e-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





