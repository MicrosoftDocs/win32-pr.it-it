---
description: Segnala che il numero corrente del flusso audio è stato modificato per il titolo principale del DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331287"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="bc97d-103">\_ \_ \_ Modifica flusso audio DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="bc97d-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="bc97d-104">Segnala che il numero corrente del flusso audio è stato modificato per il titolo principale del DVD.</span><span class="sxs-lookup"><span data-stu-id="bc97d-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc97d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc97d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc97d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bc97d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bc97d-107">Valore **DWORD** che indica il nuovo numero di flusso audio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc97d-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="bc97d-108">I numeri di flusso audio variano da 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="bc97d-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="bc97d-109">Il flusso 0xFFFFFFFF indica che non è selezionato alcun flusso.</span><span class="sxs-lookup"><span data-stu-id="bc97d-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="bc97d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bc97d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bc97d-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="bc97d-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc97d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc97d-112">Remarks</span></span>

<span data-ttu-id="bc97d-113">Il flusso audio corrente può essere modificato automaticamente con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite l'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="bc97d-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="bc97d-114">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="bc97d-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc97d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc97d-115">Requirements</span></span>



| <span data-ttu-id="bc97d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc97d-116">Requirement</span></span> | <span data-ttu-id="bc97d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bc97d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc97d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc97d-118">Header</span></span><br/> | <dl> <span data-ttu-id="bc97d-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc97d-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc97d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc97d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc97d-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="bc97d-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bc97d-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="bc97d-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bc97d-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc97d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




