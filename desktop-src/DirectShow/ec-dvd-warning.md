---
description: Segnala una condizione di avviso DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325640"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="b56c2-103">\_avviso di DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="b56c2-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="b56c2-104">Segnala una condizione di avviso DVD.</span><span class="sxs-lookup"><span data-stu-id="b56c2-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="b56c2-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b56c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b56c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b56c2-107">Valore **DWORD** che indica la condizione di avviso.</span><span class="sxs-lookup"><span data-stu-id="b56c2-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="b56c2-108">Membro del tipo di dati enumerato [**\_ avviso DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .</span><span class="sxs-lookup"><span data-stu-id="b56c2-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="b56c2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b56c2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b56c2-110">Se *pParam1* è uguale a DVD \_ Warning \_ aperto, DVD \_ Warning \_ Seek o DVD \_ Warning \_ Read, *LParam2* contiene l'ultimo codice di errore restituito da **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="b56c2-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b56c2-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b56c2-111">Requirements</span></span>



| <span data-ttu-id="b56c2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56c2-112">Requirement</span></span> | <span data-ttu-id="b56c2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b56c2-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56c2-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b56c2-114">Header</span></span><br/> | <dl> <span data-ttu-id="b56c2-115"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b56c2-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56c2-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b56c2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56c2-117">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="b56c2-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b56c2-118">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="b56c2-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b56c2-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b56c2-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




