---
description: Un'operazione è stata interrotta a causa di un errore.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8465825b93207059e5f2ea5f054deb7c3fd5619f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331635"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="a4596-103">\_ERRORABORTEX EC</span><span class="sxs-lookup"><span data-stu-id="a4596-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="a4596-104">Un'operazione è stata interrotta a causa di un errore.</span><span class="sxs-lookup"><span data-stu-id="a4596-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4596-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4596-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4596-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a4596-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a4596-107">**(HRESULT)** Codice di errore dell'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a4596-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="a4596-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a4596-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a4596-109">**(BSTR)** Stringa che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="a4596-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a4596-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="a4596-110">Default Action</span></span>

<span data-ttu-id="a4596-111">No.</span><span class="sxs-lookup"><span data-stu-id="a4596-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4596-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a4596-112">Remarks</span></span>

<span data-ttu-id="a4596-113">Il filtro [origine Windows Media](windows-media-source-filter.md) legacy Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="a4596-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="a4596-114">I nuovi filtri non devono inviare questo evento.</span><span class="sxs-lookup"><span data-stu-id="a4596-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4596-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4596-115">Requirements</span></span>



| <span data-ttu-id="a4596-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4596-116">Requirement</span></span> | <span data-ttu-id="a4596-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a4596-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4596-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4596-118">Header</span></span><br/> | <dl> <span data-ttu-id="a4596-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4596-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4596-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4596-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4596-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="a4596-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a4596-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4596-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




