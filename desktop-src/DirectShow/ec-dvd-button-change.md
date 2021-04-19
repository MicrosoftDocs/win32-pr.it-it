---
description: Segnala che il numero di pulsanti di menu DVD è stato modificato o che la selezione del pulsante è cambiata.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331109"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="0c20e-103">\_ \_ modifica pulsante DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="0c20e-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="0c20e-104">Segnala che il numero di pulsanti di menu DVD è stato modificato o che la selezione del pulsante è cambiata.</span><span class="sxs-lookup"><span data-stu-id="0c20e-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c20e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c20e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c20e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0c20e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0c20e-107">Valore **DWORD** che indica il numero di pulsanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c20e-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="0c20e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0c20e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0c20e-109">Valore **DWORD** che indica il numero di pulsante attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0c20e-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="0c20e-110">Il pulsante selezionato numero zero implica che non è selezionato alcun pulsante.</span><span class="sxs-lookup"><span data-stu-id="0c20e-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c20e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c20e-111">Remarks</span></span>

<span data-ttu-id="0c20e-112">I numeri dei pulsanti sono compresi tra 1 e 36.</span><span class="sxs-lookup"><span data-stu-id="0c20e-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="0c20e-113">Il pulsante attualmente selezionato può essere modificato automaticamente con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite l'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="0c20e-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="0c20e-114">Questo evento può segnalare qualsiasi numero di pulsanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c20e-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="0c20e-115">Questi numeri non sempre corrispondono ai numeri dei pulsanti usati per [**IDVDControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) perché tale metodo può attivare solo un subset di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0c20e-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="0c20e-116">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="0c20e-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c20e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c20e-117">Requirements</span></span>



| <span data-ttu-id="0c20e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c20e-118">Requirement</span></span> | <span data-ttu-id="0c20e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0c20e-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c20e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c20e-120">Header</span></span><br/> | <dl> <span data-ttu-id="0c20e-121"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c20e-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c20e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c20e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c20e-123">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="0c20e-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0c20e-124">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="0c20e-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0c20e-125">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0c20e-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




