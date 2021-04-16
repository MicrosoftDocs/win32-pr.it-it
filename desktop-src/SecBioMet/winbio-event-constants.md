---
title: Costanti WINBIO_EVENT (tipi WinBio \_ . h)
description: Specificare i tipi di notifiche degli eventi del provider di servizi da monitorare.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517475"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="7df9f-103">\_Costanti evento WINBIO</span><span class="sxs-lookup"><span data-stu-id="7df9f-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="7df9f-104">Le costanti seguenti possono essere utilizzate nella funzione [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) per specificare i tipi di notifiche degli eventi del provider di servizi da monitorare.</span><span class="sxs-lookup"><span data-stu-id="7df9f-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="7df9f-105">Costante</span><span class="sxs-lookup"><span data-stu-id="7df9f-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="7df9f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7df9f-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="7df9f-107"><dt>**\_evento WINBIO \_ FP non \_ recuperato**</dt></span><span class="sxs-lookup"><span data-stu-id="7df9f-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="7df9f-108">Il sensore ha rilevato una striscia da dito che non è stata richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="7df9f-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7df9f-109">Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato un dito sfiorato ma non tenta di identificare l'impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="7df9f-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="7df9f-110"><dt>**\_identificazione non \_ \_ richiesta FP dell'evento \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="7df9f-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="7df9f-111">Il sensore ha rilevato una striscia da dito che non è stata richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="7df9f-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="7df9f-112">Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="7df9f-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="7df9f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7df9f-113">Requirements</span></span>



| <span data-ttu-id="7df9f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df9f-114">Requirement</span></span> | <span data-ttu-id="7df9f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7df9f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df9f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7df9f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7df9f-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7df9f-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7df9f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7df9f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7df9f-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7df9f-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7df9f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7df9f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df9f-121"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7df9f-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df9f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7df9f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df9f-123">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="7df9f-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





