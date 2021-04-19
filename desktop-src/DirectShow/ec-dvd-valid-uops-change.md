---
description: Segnala che il set disponibile di metodi dell'interfaccia IDvdControl2 è stato modificato.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326629"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="ff9c1-103">\_ \_ \_ modifica UOPs valida DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="ff9c1-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="ff9c1-104">Segnala che il set disponibile di metodi dell'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff9c1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff9c1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff9c1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ff9c1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff9c1-107">Valore **DWORD** che contiene una combinazione di zero o più flag dall'enumerazione [**valida \_ del \_ flag UOP**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) .</span><span class="sxs-lookup"><span data-stu-id="ff9c1-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="ff9c1-108">I bit indicano quali comandi di [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono stati disabilitati in modo esplicito dal disco DVD.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="ff9c1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ff9c1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff9c1-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff9c1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff9c1-111">Remarks</span></span>

<span data-ttu-id="ff9c1-112">Questo evento indica solo le operazioni che vengono disabilitate in modo esplicito dal contenuto del disco DVD. Non garantisce che sia valido chiamare metodi che non sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="ff9c1-113">Se, ad esempio, non è presente alcun pulsante, il metodo [**IDVDControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) non funzionerà, anche se il metodo non è disabilitato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="ff9c1-114">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="ff9c1-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff9c1-115">Requirements</span></span>



| <span data-ttu-id="ff9c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff9c1-116">Requirement</span></span> | <span data-ttu-id="ff9c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ff9c1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9c1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff9c1-118">Header</span></span><br/> | <dl> <span data-ttu-id="ff9c1-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff9c1-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff9c1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff9c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9c1-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="ff9c1-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ff9c1-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="ff9c1-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ff9c1-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff9c1-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




