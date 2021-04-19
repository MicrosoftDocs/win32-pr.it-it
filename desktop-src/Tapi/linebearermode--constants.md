---
description: Le \_ costanti del flag di bit LINEBEARERMODE descrivono diverse modalità di chiamata di una chiamata.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Costanti LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332903"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="f04fc-103">\_Costanti LINEBEARERMODE</span><span class="sxs-lookup"><span data-stu-id="f04fc-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="f04fc-104">Le costanti del flag di bit **LINEBEARERMODE \_** descrivono diverse modalità di chiamata di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="f04fc-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="f04fc-105">Quando un'applicazione effettua una chiamata, può richiedere una modalità di porta di tipo specifica.</span><span class="sxs-lookup"><span data-stu-id="f04fc-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="f04fc-106">Queste modalità vengono utilizzate per selezionare una determinata qualità del servizio per la connessione richiesta dalla rete telefonica sottostante.</span><span class="sxs-lookup"><span data-stu-id="f04fc-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="f04fc-107">Le modalità di porta disponibili in una determinata riga sono una funzionalità del dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="f04fc-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="f04fc-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**\_ALTSPEECHDATA LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-109">Trasferimento alternativo di dati vocali o senza restrizioni sulla stessa chiamata (ISDN).</span><span class="sxs-lookup"><span data-stu-id="f04fc-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**\_dati LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-111">Trasferimento di dati senza restrizioni sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="f04fc-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="f04fc-112">La velocità dei dati viene specificata separatamente.</span><span class="sxs-lookup"><span data-stu-id="f04fc-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**\_multiuso LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-114">Modalità multiuso definita da ISDN.</span><span class="sxs-lookup"><span data-stu-id="f04fc-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**\_NONCALLSIGNALING LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-116">Corrisponde a una connessione non associata alla chiamata dall'applicazione al provider di servizi o allo switch (considerato come un flusso multimediale da TAPI).</span><span class="sxs-lookup"><span data-stu-id="f04fc-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**\_PassThrough LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-118">Quando una chiamata è attiva in LINEBEARERMODE \_ PassThrough, il provider di servizi fornisce accesso diretto all'hardware collegato per il controllo da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f04fc-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="f04fc-119">Questa modalità viene utilizzata principalmente dalle applicazioni che desiderano il controllo diretto temporaneo sui modem asincroni, a cui si accede tramite le [funzioni di comunicazione](/windows/desktop/DevIO/communications-functions), allo scopo di configurare o utilizzare funzionalità speciali non altrimenti supportate dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f04fc-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**\_RESTRICTEDDATA LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-121">Servizio di Bearer per i dati digitali, in cui solo i sette bit meno significativi di ogni ottetto possono contenere dati utente, ad esempio per il servizio 56Kbit/s attivato.</span><span class="sxs-lookup"><span data-stu-id="f04fc-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**\_sintesi vocale LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="f04fc-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-123">Corrisponde alla trasmissione vocale G. 711 sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="f04fc-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="f04fc-124">La rete può utilizzare tecniche di elaborazione come la trasmissione analoga, l'annullamento di Echo e la compressione/decompressione.</span><span class="sxs-lookup"><span data-stu-id="f04fc-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="f04fc-125">L'integrità dei bit non è garantita.</span><span class="sxs-lookup"><span data-stu-id="f04fc-125">Bit integrity is not assured.</span></span> <span data-ttu-id="f04fc-126">La voce non è progettata per supportare i tipi di supporto fax e modem.</span><span class="sxs-lookup"><span data-stu-id="f04fc-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f04fc-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**</span><span class="sxs-lookup"><span data-stu-id="f04fc-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f04fc-128">Si tratta di un normale servizio di porta di pari livello di 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="f04fc-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="f04fc-129">L'integrità dei bit non è garantita.</span><span class="sxs-lookup"><span data-stu-id="f04fc-129">Bit integrity is not assured.</span></span> <span data-ttu-id="f04fc-130">La voce può supportare i tipi di supporto fax e modem.</span><span class="sxs-lookup"><span data-stu-id="f04fc-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f04fc-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f04fc-131">Remarks</span></span>

<span data-ttu-id="f04fc-132">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f04fc-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="f04fc-133">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f04fc-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="f04fc-134">Si noti che la modalità di porta e il tipo di supporto sono nozioni differenti.</span><span class="sxs-lookup"><span data-stu-id="f04fc-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="f04fc-135">La modalità di connessione di una chiamata indica la qualità della connessione telefonica fornita principalmente dalla rete.</span><span class="sxs-lookup"><span data-stu-id="f04fc-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="f04fc-136">Il tipo di supporto di una chiamata indica il tipo di flusso di informazioni scambiato tramite la chiamata.</span><span class="sxs-lookup"><span data-stu-id="f04fc-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="f04fc-137">Il fax del gruppo 3 o il modem dati sono tipi di supporti che usano una chiamata con la modalità di connessione vocale a 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="f04fc-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04fc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f04fc-138">Requirements</span></span>



| <span data-ttu-id="f04fc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f04fc-139">Requirement</span></span> | <span data-ttu-id="f04fc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f04fc-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f04fc-141">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f04fc-141">TAPI version</span></span><br/> | <span data-ttu-id="f04fc-142">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f04fc-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f04fc-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f04fc-143">Header</span></span><br/>       | <dl> <span data-ttu-id="f04fc-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f04fc-144"><dt>Tapi.h</dt></span></span> </dl> |



 

