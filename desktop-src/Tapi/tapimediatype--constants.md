---
description: Le costanti di tipo supporto sono definite di seguito.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Costanti TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331769"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="83e68-103">\_Costanti TAPIMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="83e68-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="83e68-104">Sono definiti i tipi di supporto seguenti:</span><span class="sxs-lookup"><span data-stu-id="83e68-104">The following media types are defined:</span></span>



| <span data-ttu-id="83e68-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="83e68-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="83e68-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e68-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="83e68-107"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0x8</dt> audio</span><span class="sxs-lookup"><span data-stu-id="83e68-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="83e68-108">Un flusso multimediale audio che sta entrando o uscendo dal computer.</span><span class="sxs-lookup"><span data-stu-id="83e68-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="83e68-109">Un flusso multimediale di immissione viene in genere riprodotto nei relatori o inviato a un dispositivo portatile e un flusso in uscita viene in genere acquisito tramite un dispositivo microfonico o ricevitore.</span><span class="sxs-lookup"><span data-stu-id="83e68-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="83e68-110"><dt>**TAPIMEDIATYPE \_ VIDEO**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="83e68-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="83e68-111">Un flusso multimediale video che entra o esce dal computer.</span><span class="sxs-lookup"><span data-stu-id="83e68-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="83e68-112">Viene in genere eseguito il rendering di un flusso multimediale di immissione in una finestra video e un flusso multimediale in uscita viene in genere acquisito con una videocamera video.</span><span class="sxs-lookup"><span data-stu-id="83e68-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="83e68-113"><dt>**TAPIMEDIATYPE \_ 0x10 DataModel**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="83e68-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="83e68-114">Flusso multimediale dati associato a un modem dati.</span><span class="sxs-lookup"><span data-stu-id="83e68-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="83e68-115"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0x20</dt> G3FAX</span><span class="sxs-lookup"><span data-stu-id="83e68-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="83e68-116">Un flusso multimediale dati associato a un fax del protocollo G3.</span><span class="sxs-lookup"><span data-stu-id="83e68-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="83e68-117"><dt>**TAPIMEDIATYPE \_ 0x10000 multitraccia**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="83e68-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="83e68-118">Un flusso si trova in un terminale multitraccia.</span><span class="sxs-lookup"><span data-stu-id="83e68-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="83e68-119"><dt>**\_ \_ Flusso singolo RTP \_ MEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="83e68-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="83e68-120">Questo GUID viene usato tra un terminale fornito dall'applicazione e il flusso del MSP.</span><span class="sxs-lookup"><span data-stu-id="83e68-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="83e68-121">Se il pin del terminale supporta questo tipo di supporto, il flusso effettuerà lo scambio di dati RTP non elaborati con il terminale.</span><span class="sxs-lookup"><span data-stu-id="83e68-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="83e68-122">Questa modalità è supportata solo dai flussi video in H323 MSP e IPConf MSP per Windows 2000 SP1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="83e68-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="83e68-123">**Intestazione:** Dichiarata in ipmsp. h.</span><span class="sxs-lookup"><span data-stu-id="83e68-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="83e68-124">L'intestazione ipmsp. h non è disponibile in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83e68-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="83e68-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e68-125">Requirements</span></span>



| <span data-ttu-id="83e68-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e68-126">Requirement</span></span> | <span data-ttu-id="83e68-127">Valore</span><span class="sxs-lookup"><span data-stu-id="83e68-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83e68-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="83e68-128">TAPI version</span></span><br/> | <span data-ttu-id="83e68-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="83e68-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="83e68-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e68-130">Header</span></span><br/>       | <dl> <span data-ttu-id="83e68-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e68-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e68-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83e68-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e68-133">**ITQOSEvent:: Get \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="83e68-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="83e68-134">**ITAMMediaFormat:: Get \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="83e68-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="83e68-135">**ITAMMediaFormat::p UT \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="83e68-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="83e68-136">**ITCallInfo:: Get \_ CallInfoLong**</span><span class="sxs-lookup"><span data-stu-id="83e68-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="83e68-137">**ITMediaSupport:: Get \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="83e68-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="83e68-138">**ITTerminalSupport::CreateTerminal**</span><span class="sxs-lookup"><span data-stu-id="83e68-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

