---
title: Comando MCI_SETVIDEO (mmsystem. h)
description: Il \_ comando MCI sevideo imposta i valori associati alla riproduzione video. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Comando MCI_SETVIDEO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476882"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="0a982-105">\_Comando MCI SEvideo</span><span class="sxs-lookup"><span data-stu-id="0a982-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="0a982-106">Il \_ comando MCI sevideo imposta i valori associati alla riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="0a982-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="0a982-107">I dispositivi Digital-video e VCR riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="0a982-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="0a982-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a982-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="0a982-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a982-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a982-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0a982-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0a982-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="0a982-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0a982-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0a982-113">**MCI \_ NOTIFICA**, **MCI \_ wait** o **MCI \_ test**.</span><span class="sxs-lookup"><span data-stu-id="0a982-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="0a982-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0a982-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a982-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span><span class="sxs-lookup"><span data-stu-id="0a982-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="0a982-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0a982-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0a982-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a982-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a982-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a982-118">Return Value</span></span>

<span data-ttu-id="0a982-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="0a982-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a982-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a982-120">Remarks</span></span>

<span data-ttu-id="0a982-121">Con il tipo di dispositivo "digitalvideo" vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="0a982-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ video \_ ALG</span><span class="sxs-lookup"><span data-stu-id="0a982-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="0a982-123">Il membro **lpstrAlgorithm** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer contenente il nome di un algoritmo di compressione video.</span><span class="sxs-lookup"><span data-stu-id="0a982-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="0a982-124">L'algoritmo di compressione viene usato dai comandi di [ \_ riserva MCI](mci-reserve.md) o del [ \_ record MCI](mci-record.md) successivi.</span><span class="sxs-lookup"><span data-stu-id="0a982-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="0a982-125">Gli algoritmi disponibili sono dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a982-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="0a982-126">Se l'algoritmo specificato non è compatibile con il formato di file corrente, il formato del file viene modificato nel formato predefinito per l'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="0a982-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>CLOCKTIME DGV di MCI- \_ \_ video \_</span><span class="sxs-lookup"><span data-stu-id="0a982-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="0a982-128">Se usato con **MCI \_ DGV \_ video \_ over**, indica che l'ora è specificata in millisecondi ed è il tempo assoluto.</span><span class="sxs-lookup"><span data-stu-id="0a982-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="0a982-129">Questa volta non è al passo con la riproduzione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0a982-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="0a982-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_ \_ input video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="0a982-131">Modifica la **\_ \_ \_ luminosità del video MCI DGV**, **MCI \_ DGV \_ sevideo \_ color**, **MCI \_ DGV \_ sevideo \_ Contrast**, **MCI \_ DGV \_ \_** sevideo gamma, **MCI \_ DGV \_ sevideo \_ nitidity** o **MCI \_ DGV \_ sevideo \_ tinte** in modo che influisca sul segnale di input e modifichi gli elementi registrati.</span><span class="sxs-lookup"><span data-stu-id="0a982-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="0a982-132">Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="0a982-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_elemento DGV del \_ video \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="0a982-134">Una costante video viene specificata nel membro **dwItem** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-135">La costante identifica il valore che viene impostato.</span><span class="sxs-lookup"><span data-stu-id="0a982-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="0a982-136">Con questo flag è possibile specificare le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="0a982-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procedura di \_ estrazione del \_ video \_ di MCI AVI</span><span class="sxs-lookup"><span data-stu-id="0a982-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-138">Un nuovo indirizzo della procedura di disegno viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-139">È possibile specificare una nuova procedura di disegno solo quando il dispositivo è inattivo.</span><span class="sxs-lookup"><span data-stu-id="0a982-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="0a982-140">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="0a982-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="0a982-141">Non esiste alcun equivalente a questo flag nell'interfaccia del comando di stringa.</span><span class="sxs-lookup"><span data-stu-id="0a982-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_ \_ \_ colore tavolozza video di MCI AVI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="0a982-143">Un nuovo colore della tavolozza viene specificato nei membri **dwOver** e **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-144">Il membro **dwOver** specifica l'indice della tavolozza del colore da modificare e il membro **dwValue** specifica il nuovo colore come valore RGB.</span><span class="sxs-lookup"><span data-stu-id="0a982-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="0a982-145">Quando si usa questa costante, è necessario specificare anche i flag di valore **\_ DGV \_ \_** di MCI DGV e i flag di **\_ \_ \_ valore video** di MCI con la **\_ \_ \_ voce MCI DGV** .</span><span class="sxs-lookup"><span data-stu-id="0a982-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="0a982-146">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="0a982-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_mezzitoni della \_ tavolozza del video MCI AVI \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a982-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-148">Indica che deve essere utilizzata la tavolozza dei mezzitoni, anziché la tavolozza predefinita.</span><span class="sxs-lookup"><span data-stu-id="0a982-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="0a982-149">Questo flag viene riconosciuto solo dal driver Digital-video MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="0a982-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>BITSPERPEL DGV di MCI- \_ \_ video \_</span><span class="sxs-lookup"><span data-stu-id="0a982-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="0a982-151">Il numero di bit per pixel è specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-152">Il numero di bit per pixel viene usato per salvare i dati acquisiti o registrati</span><span class="sxs-lookup"><span data-stu-id="0a982-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="0a982-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_luminosità del \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="0a982-154">Il livello di luminosità del video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_colore del \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="0a982-156">Il livello di saturazione dei colori video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_contrasto del \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="0a982-158">Il livello di contrasto video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_ \_ \_ frequenza dei FOTOgrammi DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-160">Viene specificata una frequenza dei fotogrammi nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-161">La frequenza viene specificata in unità di fotogrammi al secondo per 1000.</span><span class="sxs-lookup"><span data-stu-id="0a982-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="0a982-162">Ad esempio, 29,97 frame al secondo viene specificato come 29970.</span><span class="sxs-lookup"><span data-stu-id="0a982-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_gamma di \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="0a982-164">Un valore dell'esponente di correzione gamma viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-165">La correzione gamma regola il mapping tra l'intensità codificata nell'origine della presentazione e la luminosità visualizzata.</span><span class="sxs-lookup"><span data-stu-id="0a982-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="0a982-166">Il valore è l'esponente moltiplicato per 1000.</span><span class="sxs-lookup"><span data-stu-id="0a982-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="0a982-167">2200, ad esempio, indica un esponente di 2,2.</span><span class="sxs-lookup"><span data-stu-id="0a982-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="0a982-168">Il valore 1000 indica un esponente di 1, che non applica alcuna correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="0a982-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_colore della \_ chiave DGV del video MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a982-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="0a982-170">Il colore della chiave viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-171">Il colore della chiave è un valore RGB.</span><span class="sxs-lookup"><span data-stu-id="0a982-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_ \_ \_ indice chiave video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="0a982-173">Il valore di indice della chiave viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-174">Il parametro di indice è un indice della tavolozza fisica.</span><span class="sxs-lookup"><span data-stu-id="0a982-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>PALHANDLE DGV di MCI- \_ \_ video \_</span><span class="sxs-lookup"><span data-stu-id="0a982-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-176">Un handle della tavolozza viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-177">L'handle della tavolozza è contenuto nella parola di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="0a982-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="0a982-178">I dispositivi digitali video non devono liberare la tavolozza passata con questo comando.</span><span class="sxs-lookup"><span data-stu-id="0a982-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="0a982-179">Le applicazioni devono liberarsi dopo la chiusura del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a982-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="0a982-180">Questo flag è supportato solo dai dispositivi che utilizzano tavolozze.</span><span class="sxs-lookup"><span data-stu-id="0a982-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="0a982-181">Se questo handle della tavolozza specificato è zero, viene utilizzata la tavolozza predefinita.</span><span class="sxs-lookup"><span data-stu-id="0a982-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_ \_ nitidezza video MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="0a982-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="0a982-183">Un valore di nitidezza del video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_ \_ origine video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-185">Una costante che specifica l'origine dell'input video è specificata nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-186">Sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-186">The following constants are defined:</span></span>

-   <span data-ttu-id="0a982-187">**MCI \_ DGV \_ video \_ src \_ NTSC**: NTSC Television.</span><span class="sxs-lookup"><span data-stu-id="0a982-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="0a982-188">MCI \_ DGV \_ video \_ src \_ PAL: PAL Television.</span><span class="sxs-lookup"><span data-stu-id="0a982-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="0a982-189">MCI \_ DGV video \_ \_ src \_ RGB: video RGB.</span><span class="sxs-lookup"><span data-stu-id="0a982-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="0a982-190">MCI \_ DGV \_ video \_ src \_ SECAM: SECAM Television.</span><span class="sxs-lookup"><span data-stu-id="0a982-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="0a982-191">MCI \_ DGV video \_ \_ src \_ SVIDEO: S-video.</span><span class="sxs-lookup"><span data-stu-id="0a982-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flusso DGV del \_ video \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="0a982-193">Un flusso video viene specificato nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-194">Il valore integer specifica il flusso video riprodotto dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0a982-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="0a982-195">Se il flusso non è specificato e il formato del file non definisce un flusso predefinito, viene riprodotto il primo flusso video con interfoliazione fisico.</span><span class="sxs-lookup"><span data-stu-id="0a982-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_ \_ tinta del video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="0a982-197">Un valore di tinta video viene specificato come fattore nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-198">In genere, questa regolazione viene modellata dopo il controllo della tinta di molti set di televisori dei colori, con 250 definito come verde, 750 definito come rosso e 0 (o 1000) definito come blu.</span><span class="sxs-lookup"><span data-stu-id="0a982-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="0a982-199">Il valore nominale è sempre 500.</span><span class="sxs-lookup"><span data-stu-id="0a982-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_output del \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="0a982-201">La **\_ \_ \_ luminosità del video MCI DGV**, **MCI \_ DGV \_ sevideo \_ color**, **MCI \_ DGV \_ sevideo \_ Contrast**, **MCI \_ DGV \_ \_** sevideo gamma, **MCI \_ DGV \_ sevideo \_ nitidity** o **MCI \_ DGV \_ sevideo \_ tinte** flag viene modificato in modo che influisca solo sul segnale visualizzato e non su ciò che viene registrato.</span><span class="sxs-lookup"><span data-stu-id="0a982-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="0a982-202">Se possibile, si tratta dell'impostazione predefinita durante il monitoraggio di un file.</span><span class="sxs-lookup"><span data-stu-id="0a982-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>DGV di MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0a982-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="0a982-204">Un parametro della lunghezza della transizione è incluso nel membro **dwOver** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-205">La lunghezza della transizione specifica la durata (nel formato dell'ora corrente) che deve essere necessaria per apportare una modifica.</span><span class="sxs-lookup"><span data-stu-id="0a982-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="0a982-206">Se questo flag non viene utilizzato, la modifica viene eseguita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0a982-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_qualità del \_ video DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="0a982-208">Il membro **lpstrQuality** della struttura identificata da *lpSetVideo* contiene un indirizzo di un buffer che descrive la qualità del video.</span><span class="sxs-lookup"><span data-stu-id="0a982-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="0a982-209">Una stringa di testo nel buffer specifica le caratteristiche dell'algoritmo di compressione video.</span><span class="sxs-lookup"><span data-stu-id="0a982-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="0a982-210">Per selezionare un descrittore di qualità per l'algoritmo specificato, è possibile usare il flag **MCI \_ DGV \_ sevideo \_ ALG** .</span><span class="sxs-lookup"><span data-stu-id="0a982-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="0a982-211">Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="0a982-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="0a982-212">Gli algoritmi e i nomi dei descrittori disponibili dipendono dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a982-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="0a982-213">Ogni dispositivo fornisce la documentazione per gli algoritmi disponibili e una descrizione dei nomi di descrittori applicabili.</span><span class="sxs-lookup"><span data-stu-id="0a982-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="0a982-214">Il comando [MCI \_ Quality](mci-quality.md) può definire nomi di descrittori aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="0a982-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="0a982-215">Tutti i dispositivi supportano i descrittori "low", "medium" e "High".</span><span class="sxs-lookup"><span data-stu-id="0a982-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="0a982-216">Il valore predefinito è specifico del driver.</span><span class="sxs-lookup"><span data-stu-id="0a982-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_ \_ record video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="0a982-218">Specifica se la registrazione include o esclude i dati video.</span><span class="sxs-lookup"><span data-stu-id="0a982-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="0a982-219">In combinazione con **MCI \_ impostato \_ su**, i dati video vengono registrati.</span><span class="sxs-lookup"><span data-stu-id="0a982-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="0a982-220">Se combinato con **MCI \_ impostato su \_ disattivato**, i dati video vengono esclusi.</span><span class="sxs-lookup"><span data-stu-id="0a982-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="0a982-221">Il valore predefinito include i dati video.</span><span class="sxs-lookup"><span data-stu-id="0a982-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ numero src del video \_ DGV \_ di MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="0a982-223">Un numero per l'origine video viene specificato nel membro **dwSourceNumber** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-224">Se è presente più di un input del tipo specificato dal **\_ \_ \_ valore DGV di MCI**, il valore seleziona l'input.</span><span class="sxs-lookup"><span data-stu-id="0a982-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="0a982-225">Questo flag deve essere sempre utilizzato con **l' \_ \_ \_ origine DGV di MCI**.</span><span class="sxs-lookup"><span data-stu-id="0a982-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="0a982-226">Se **il \_ \_ \_ valore DGV di MCI** viene omesso, tuttavia, il numero di origine specificato indica l'origine assoluta da usare come specificato nel [comando \_ elenco MCI](mci-list.md) .</span><span class="sxs-lookup"><span data-stu-id="0a982-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>DGV di MCI- \_ \_ video \_ ancora</span><span class="sxs-lookup"><span data-stu-id="0a982-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="0a982-228">Il nome dell'algoritmo o il valore di qualità specificato si applica alle immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="0a982-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="0a982-229">Ogni driver di dispositivo deve supportare un algoritmo di "None", che significa nessuna compressione.</span><span class="sxs-lookup"><span data-stu-id="0a982-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="0a982-230">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0a982-230">This is the default.</span></span> <span data-ttu-id="0a982-231">In questo caso, i dispositivi digitali video salvano le immagini ancora come bitmap indipendenti dal dispositivo RGB.</span><span class="sxs-lookup"><span data-stu-id="0a982-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="0a982-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valore video DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-233">Un valore è incluso nel membro **dwValue** della struttura identificata da *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="0a982-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="0a982-234">Il significato del valore è specificato dal flag dell' **\_ \_ \_ elemento DGV di MCI** .</span><span class="sxs-lookup"><span data-stu-id="0a982-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>\_set \_ disattivato</span><span class="sxs-lookup"><span data-stu-id="0a982-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="0a982-236">Disabilita l'output del video.</span><span class="sxs-lookup"><span data-stu-id="0a982-236">Disables video output.</span></span> <span data-ttu-id="0a982-237">Per i dispositivi digitali video, la disabilitazione del video imposta i pixel nel rettangolo di destinazione definito dal comando [MCI \_ put](mci-put.md) (o il relativo valore predefinito, l'area client della finestra corrente) su un colore a tinta unita, ma non ha alcun effetto sul buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="0a982-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="0a982-238">Se lo si desidera, è possibile nascondere la finestra con il comando della [ \_ finestra MCI](mci-window.md) .</span><span class="sxs-lookup"><span data-stu-id="0a982-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="0a982-239">L'origine del video, sia che si tratti di un'area di lavoro o di un input esterno, potrebbe continuare a archiviare nuove immagini nel buffer frame, ma non vengono visualizzate finché il video non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="0a982-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="0a982-240">Sebbene le applicazioni usino il \_ comando MCI sevideo per controllare questa funzione, i dispositivi video digitali devono ancora supportare questo flag.</span><span class="sxs-lookup"><span data-stu-id="0a982-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="0a982-241">Il valore predefinito dopo l'apertura è on.</span><span class="sxs-lookup"><span data-stu-id="0a982-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ impostato \_ su</span><span class="sxs-lookup"><span data-stu-id="0a982-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="0a982-243">Abilita l'output del video.</span><span class="sxs-lookup"><span data-stu-id="0a982-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="0a982-244">Per i dispositivi digitali video, il parametro *lpSetVideo* punta a una [**struttura \_ DGV \_ \_ parametri di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="0a982-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="0a982-245">Con il tipo di dispositivo "VCR" vengono usati i flag aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="0a982-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_ \_ record video MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="0a982-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="0a982-247">Imposta la registrazione video su on o off.</span><span class="sxs-lookup"><span data-stu-id="0a982-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="0a982-248">Usato insieme a uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="0a982-249">**MCI \_ IMPOSTA \_ su**.</span><span class="sxs-lookup"><span data-stu-id="0a982-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="0a982-250">Registrazione video su.</span><span class="sxs-lookup"><span data-stu-id="0a982-250">Video recording on.</span></span>
-   <span data-ttu-id="0a982-251">**MCI \_ IMPOSTARE \_ disattivato**.</span><span class="sxs-lookup"><span data-stu-id="0a982-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="0a982-252">Registrazione video disattivata.</span><span class="sxs-lookup"><span data-stu-id="0a982-252">Video recording off.</span></span> <span data-ttu-id="0a982-253">Prima di disattivare la registrazione video, potrebbe essere necessario disattivare la registrazione di assemblaggio (usando il comando [MCI \_ set](mci-set.md) con il flag **MCI \_ \_ set \_ assembla \_ record** impostato su OFF).</span><span class="sxs-lookup"><span data-stu-id="0a982-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_traccia MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="0a982-255">Il membro **dwTrack** della struttura identificata da *lpSetVideo* specifica la traccia interessata dal comando.</span><span class="sxs-lookup"><span data-stu-id="0a982-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_ \_ origine video VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="0a982-257">Imposta l'origine video e deve essere usata con il **\_ \_ sevideo MCI VCR \_ per** contrassegnare.</span><span class="sxs-lookup"><span data-stu-id="0a982-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_ \_ monitoraggio video VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="0a982-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="0a982-259">Imposta il monitoraggio origine video e deve essere usato con il \_ \_ sevideo MCI VCR \_ per contrassegnare.</span><span class="sxs-lookup"><span data-stu-id="0a982-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="0a982-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_video MCI VCR \_ \_ in</span><span class="sxs-lookup"><span data-stu-id="0a982-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="0a982-261">Il membro **dwTo** della struttura identificata da *lpSetVideo* contiene una delle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a982-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="0a982-262">**\_Tuner di \_ \_ tipo src VCR di \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="0a982-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="0a982-263">**\_ \_ \_ riga tipo src VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="0a982-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="0a982-264">**\_ \_ tipo src VCR \_ MCI \_ aux**</span><span class="sxs-lookup"><span data-stu-id="0a982-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="0a982-265">**\_ \_ tipo src VCR \_ MCI \_ generico**</span><span class="sxs-lookup"><span data-stu-id="0a982-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="0a982-266">**\_silenziamento del \_ \_ tipo src del VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="0a982-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="0a982-267">**\_ \_ \_ output tipo src VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="0a982-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="0a982-268">**\_tipo src del VCR MCI \_ \_ \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="0a982-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="0a982-269">**\_numero di \_ video VCR \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="0a982-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="0a982-270">Il membro **dwNumber** della struttura identificata da *lpSetVideo* contiene l'input video, del tipo specificato nel membro **dwTo** , da usare.</span><span class="sxs-lookup"><span data-stu-id="0a982-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="0a982-271">Per i dispositivi VCR, il parametro *lpSetVideo* punta a una struttura [**\_ \_ \_ parametri del videoregistratore MCI**](mci-vcr-setvideo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0a982-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a982-272">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a982-272">Requirements</span></span>



| <span data-ttu-id="0a982-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a982-273">Requirement</span></span> | <span data-ttu-id="0a982-274">Valore</span><span class="sxs-lookup"><span data-stu-id="0a982-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a982-275">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a982-275">Minimum supported client</span></span><br/> | <span data-ttu-id="0a982-276">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a982-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a982-277">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a982-277">Minimum supported server</span></span><br/> | <span data-ttu-id="0a982-278">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a982-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a982-279">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a982-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a982-280"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a982-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a982-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a982-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a982-282">MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0a982-283">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="0a982-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

