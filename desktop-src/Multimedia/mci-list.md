---
title: Comando MCI_LIST (mmsystem. h)
description: Il \_ comando MCI List ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Comando MCI_LIST Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519036"
---
# <a name="mci_list-command"></a><span data-ttu-id="74681-105">\_Comando elenco MCI</span><span class="sxs-lookup"><span data-stu-id="74681-105">MCI\_LIST command</span></span>

<span data-ttu-id="74681-106">Il \_ comando MCI List ottiene informazioni sul numero e sui tipi di input disponibili per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74681-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="74681-107">I dispositivi Digital-video e VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="74681-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="74681-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="74681-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="74681-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="74681-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74681-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="74681-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="74681-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="74681-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="74681-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="74681-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="74681-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="74681-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="74681-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="74681-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="74681-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span><span class="sxs-lookup"><span data-stu-id="74681-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="74681-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="74681-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="74681-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74681-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74681-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74681-118">Return Value</span></span>

<span data-ttu-id="74681-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="74681-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="74681-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="74681-120">Remarks</span></span>

<span data-ttu-id="74681-121">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="74681-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="74681-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>\_elenco DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="74681-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="74681-123">Il membro **lpstrAlgorithm** della struttura identificata da *lpList* contiene un indirizzo di un buffer contenente il nome di un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="74681-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="74681-124">Il nome viene usato per recuperare i tipi di descrittori di qualità associati a un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="74681-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="74681-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_ \_ conteggio elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="74681-126">Restituisce il numero di opzioni del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="74681-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="74681-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_ \_ elemento elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="74681-128">Costante che indica che il tipo di elenco è incluso nel membro **dwItem** della struttura identificata da *lpList*.</span><span class="sxs-lookup"><span data-stu-id="74681-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="74681-129">Questo flag è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="74681-129">This flag is required.</span></span> <span data-ttu-id="74681-130">Utilizzare una delle seguenti costanti per indicare il tipo di elenco:</span><span class="sxs-lookup"><span data-stu-id="74681-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="74681-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ List \_ audio \_ ALG</span><span class="sxs-lookup"><span data-stu-id="74681-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="74681-132">Il comando deve recuperare i nomi degli algoritmi audio.</span><span class="sxs-lookup"><span data-stu-id="74681-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="74681-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_ \_ \_ qualità audio elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="74681-134">Il comando deve recuperare i livelli di qualità audio.</span><span class="sxs-lookup"><span data-stu-id="74681-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="74681-135">I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*.</span><span class="sxs-lookup"><span data-stu-id="74681-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="74681-136">Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="74681-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="74681-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_ \_ \_ flusso audio elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="74681-138">Il comando deve recuperare i nomi dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="74681-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="74681-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_elenco DGV \_ MCI \_ ancora \_ al</span><span class="sxs-lookup"><span data-stu-id="74681-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="74681-140">Il comando deve recuperare i nomi degli algoritmi ancora.</span><span class="sxs-lookup"><span data-stu-id="74681-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="74681-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>\_elenco DGV di MCI \_ \_ ancora \_ qualità</span><span class="sxs-lookup"><span data-stu-id="74681-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="74681-142">Il comando deve recuperare i livelli qualitativi.</span><span class="sxs-lookup"><span data-stu-id="74681-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="74681-143">I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*.</span><span class="sxs-lookup"><span data-stu-id="74681-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="74681-144">Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="74681-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="74681-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>VIDEO di MCI \_ DGV \_ List \_ \_ ALG</span><span class="sxs-lookup"><span data-stu-id="74681-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="74681-146">Il comando deve recuperare i nomi degli algoritmi video.</span><span class="sxs-lookup"><span data-stu-id="74681-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="74681-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_ \_ \_ qualità video elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="74681-148">Il comando deve recuperare i livelli di qualità del video.</span><span class="sxs-lookup"><span data-stu-id="74681-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="74681-149">I livelli restituiti sono associati all'algoritmo a cui fa riferimento il membro **lpstrAlgorithm** della struttura identificata da *lpList*.</span><span class="sxs-lookup"><span data-stu-id="74681-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="74681-150">Se tale membro viene specificato utilizzando la stringa "Current", vengono restituite le qualità associate all'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="74681-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="74681-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_ \_ \_ origine video elenco DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="74681-152">Il comando deve restituire informazioni sulle origini video.</span><span class="sxs-lookup"><span data-stu-id="74681-152">The command should return information about the video sources.</span></span> <span data-ttu-id="74681-153">Quando viene usato con \_ il \_ \_ numero di elenchi DGV di MCI, il comando restituisce il numero di origini video.</span><span class="sxs-lookup"><span data-stu-id="74681-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="74681-154">Se usato con il \_ \_ \_ numero di elenco DGV di MCI, il comando restituisce il tipo di un'origine video.</span><span class="sxs-lookup"><span data-stu-id="74681-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="74681-155">MCI definisce i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="74681-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="74681-156">MCI \_ DGV \_ sevideo \_ src \_ Generic</span><span class="sxs-lookup"><span data-stu-id="74681-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="74681-157">MCI \_ DGV \_ video \_ src \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="74681-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="74681-158">DGV di MCI \_ \_ video \_ src \_ PAL</span><span class="sxs-lookup"><span data-stu-id="74681-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="74681-159">MCI \_ DGV \_ video \_ src \_ RGB</span><span class="sxs-lookup"><span data-stu-id="74681-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="74681-160">MCI \_ DGV \_ video \_ src \_ SECAM</span><span class="sxs-lookup"><span data-stu-id="74681-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="74681-161">MCI \_ DGV \_ video \_ src \_ SVIDEO</span><span class="sxs-lookup"><span data-stu-id="74681-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="74681-162">Potrebbe essere restituita più di un'origine di ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="74681-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="74681-163">Il tipo di origine generico viene usato quando è consentito più di un tipo di segnale per quel connettore.</span><span class="sxs-lookup"><span data-stu-id="74681-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="74681-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_ \_ flusso video dell'elenco DGV \_ di \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="74681-165">Il comando deve recuperare i nomi dei flussi video.</span><span class="sxs-lookup"><span data-stu-id="74681-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="74681-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_numero di \_ elenco \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="74681-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="74681-167">Un indice viene specificato nel membro **dwNumber** della struttura identificata da *lpList*.</span><span class="sxs-lookup"><span data-stu-id="74681-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="74681-168">L'indice deve essere un numero intero compreso tra 1 e il valore restituito per \_ il \_ flag di conteggio DGV elenco MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="74681-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="74681-169">Per i dispositivi digitali video, *lpList* punta a una [**struttura \_ DGV \_ elenco \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="74681-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="74681-170">I flag aggiuntivi seguenti si applicano al tipo di dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="74681-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="74681-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_ \_ \_ origine audio elenco VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="74681-172">Elenca gli input o i tipi audio.</span><span class="sxs-lookup"><span data-stu-id="74681-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="74681-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_ \_ conteggio elenco VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="74681-174">Imposta il membro **dwReturn** della struttura identificata da *lpList* sul numero totale di input video o audio.</span><span class="sxs-lookup"><span data-stu-id="74681-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="74681-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>\_numero di \_ elenco \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="74681-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="74681-176">Imposta il membro **dwReturn** della struttura identificata da *lpList* sul tipo di input video o audio specificato dal membro **dwNumber** .</span><span class="sxs-lookup"><span data-stu-id="74681-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="74681-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_ \_ \_ origine video elenco VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="74681-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="74681-178">Elenca gli input o i tipi di video.</span><span class="sxs-lookup"><span data-stu-id="74681-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="74681-179">Per i dispositivi VCR, *lpList* punta a una struttura [**\_ \_ \_ parametri elenco VCR MCI**](mci-vcr-list-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="74681-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="74681-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74681-180">Requirements</span></span>



| <span data-ttu-id="74681-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="74681-181">Requirement</span></span> | <span data-ttu-id="74681-182">Valore</span><span class="sxs-lookup"><span data-stu-id="74681-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74681-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74681-183">Minimum supported client</span></span><br/> | <span data-ttu-id="74681-184">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74681-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74681-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74681-185">Minimum supported server</span></span><br/> | <span data-ttu-id="74681-186">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74681-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74681-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74681-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="74681-188"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74681-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74681-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74681-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74681-190">MCI</span><span class="sxs-lookup"><span data-stu-id="74681-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="74681-191">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="74681-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

