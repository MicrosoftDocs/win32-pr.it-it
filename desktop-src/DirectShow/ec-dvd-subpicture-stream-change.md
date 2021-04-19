---
description: Segnala che il numero del flusso di sottoimmagine corrente è stato modificato per il titolo principale.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326637"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="39f76-103">\_ \_ Modifica flusso di sottoimmagine DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="39f76-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="39f76-104">Segnala che il numero del flusso di sottoimmagine corrente è stato modificato per il titolo principale.</span><span class="sxs-lookup"><span data-stu-id="39f76-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="39f76-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="39f76-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f76-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="39f76-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="39f76-107">Valore **DWORD** che indica il nuovo numero di flusso di sottoimmagine utente.</span><span class="sxs-lookup"><span data-stu-id="39f76-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="39f76-108">I numeri di flusso di immagini secondarie sono compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="39f76-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="39f76-109">Il flusso 0xFFFFFFFF indica che non è selezionato alcun flusso.</span><span class="sxs-lookup"><span data-stu-id="39f76-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="39f76-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="39f76-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="39f76-111">Valore booleano che indica lo stato on/off dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="39f76-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39f76-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="39f76-112">Remarks</span></span>

<span data-ttu-id="39f76-113">È possibile modificare automaticamente la sottoimmagine con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span><span class="sxs-lookup"><span data-stu-id="39f76-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="39f76-114">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="39f76-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f76-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39f76-115">Requirements</span></span>



| <span data-ttu-id="39f76-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39f76-116">Requirement</span></span> | <span data-ttu-id="39f76-117">Valore</span><span class="sxs-lookup"><span data-stu-id="39f76-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f76-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39f76-118">Header</span></span><br/> | <dl> <span data-ttu-id="39f76-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39f76-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f76-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39f76-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f76-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="39f76-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="39f76-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="39f76-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="39f76-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="39f76-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




