---
description: Segnala una condizione di errore DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326657"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="39bf1-103">\_errore DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="39bf1-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="39bf1-104">Segnala una condizione di errore DVD.</span><span class="sxs-lookup"><span data-stu-id="39bf1-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="39bf1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="39bf1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bf1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="39bf1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="39bf1-107">Valore **DWORD** che indica la condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="39bf1-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="39bf1-108">Membro del tipo di dati enumerato [**\_ errore DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="39bf1-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="39bf1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="39bf1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="39bf1-110">Il significato dipende dal valore di *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="39bf1-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="39bf1-111">Per ulteriori informazioni, vedere l' [**\_ errore DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="39bf1-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39bf1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="39bf1-112">Remarks</span></span>

<span data-ttu-id="39bf1-113">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="39bf1-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bf1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39bf1-114">Requirements</span></span>



| <span data-ttu-id="39bf1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bf1-115">Requirement</span></span> | <span data-ttu-id="39bf1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="39bf1-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39bf1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39bf1-117">Header</span></span><br/> | <dl> <span data-ttu-id="39bf1-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39bf1-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39bf1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39bf1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bf1-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="39bf1-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="39bf1-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="39bf1-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="39bf1-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="39bf1-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




