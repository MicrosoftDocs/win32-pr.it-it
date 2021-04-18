---
description: Segnala l'ora corrente, in \_ \_ formato di timecode HMSF DVD, rispetto all'inizio del titolo. Questo evento viene generato all'inizio di ogni VOBU, che si verifica ogni 0,4 e 1,0 secondi.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325186"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="1cba5-104">\_ \_ \_ ora HMSF corrente del DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="1cba5-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="1cba5-105">Segnala l'ora corrente, in formato di [**\_ \_ timecode HMSF DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) , rispetto all'inizio del titolo.</span><span class="sxs-lookup"><span data-stu-id="1cba5-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="1cba5-106">Questo evento viene generato all'inizio di ogni VOBU, che si verifica ogni 0,4 e 1,0 secondi.</span><span class="sxs-lookup"><span data-stu-id="1cba5-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cba5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cba5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cba5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1cba5-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1cba5-109">Valore ULONG che contiene la struttura del \_ timecode HMSF DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="1cba5-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="1cba5-110">Assegnare lParam1 a una variabile ULONG, quindi eseguire il cast della variabile in \_ un \_ timecode DVD HMSF per accedere ai valori.</span><span class="sxs-lookup"><span data-stu-id="1cba5-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="1cba5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1cba5-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1cba5-112">Valore ULONG contenente un'Unione di [**flag del \_ timecode \_ del DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span><span class="sxs-lookup"><span data-stu-id="1cba5-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cba5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cba5-113">Remarks</span></span>

<span data-ttu-id="1cba5-114">Il \_ formato del timecode DVD HMSF \_ è destinato a sostituire il vecchio formato BCD restituito negli eventi dell' \_ ora corrente del DVD EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cba5-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="1cba5-115">I timecode HMSF sono più facili da usare.</span><span class="sxs-lookup"><span data-stu-id="1cba5-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="1cba5-116">Per fare in modo che lo strumento di navigazione invii gli \_ \_ eventi del \_ tempo HMSF corrente del DVD EC \_ anziché \_ gli eventi dell'ora corrente del DVD EC \_ \_ , un'applicazione deve chiamare `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="1cba5-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="1cba5-117">Quando questo flag è impostato, lo strumento di spostamento prevede anche che tutti i parametri di tempo nei metodi [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) vengano passati come \_ timecode HMSF del DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="1cba5-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="1cba5-118">Questo evento viene generato nei domini del titolo.</span><span class="sxs-lookup"><span data-stu-id="1cba5-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cba5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cba5-119">Requirements</span></span>



| <span data-ttu-id="1cba5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cba5-120">Requirement</span></span> | <span data-ttu-id="1cba5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1cba5-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cba5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cba5-122">Header</span></span><br/> | <dl> <span data-ttu-id="1cba5-123"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cba5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cba5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cba5-125">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="1cba5-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1cba5-126">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="1cba5-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1cba5-127">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1cba5-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




