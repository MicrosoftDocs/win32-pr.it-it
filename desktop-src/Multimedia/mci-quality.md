---
title: Comando MCI_QUALITY (mmsystem. h)
description: Il \_ comando di qualità MCI definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Comando MCI_QUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400222"
---
# <a name="mci_quality-command"></a><span data-ttu-id="6abcd-105">\_Comando qualità MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="6abcd-106">Il \_ comando di qualità MCI definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua.</span><span class="sxs-lookup"><span data-stu-id="6abcd-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="6abcd-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="6abcd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6abcd-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="6abcd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="6abcd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6abcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abcd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6abcd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="6abcd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6abcd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6abcd-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6abcd-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6abcd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span><span class="sxs-lookup"><span data-stu-id="6abcd-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-116">Puntatore a una [**struttura \_ \_ \_ parametri di qualità DGV di MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="6abcd-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abcd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6abcd-117">Return Value</span></span>

<span data-ttu-id="6abcd-118">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6abcd-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abcd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6abcd-119">Remarks</span></span>

<span data-ttu-id="6abcd-120">Il nome definito per questo livello di qualità può essere utilizzato quando si imposta la qualità audio, video o ancora con i comandi [MCI \_ sefonica](mci-setaudio.md) e [MCI \_ sevideo](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="6abcd-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="6abcd-121">I flag aggiuntivi seguenti si applicano ai dispositivi digitali video:</span><span class="sxs-lookup"><span data-stu-id="6abcd-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="6abcd-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_qualità MCI \_ ALG</span><span class="sxs-lookup"><span data-stu-id="6abcd-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-123">Il membro **lpstrAlgorithm** della struttura identificata da *lpQuality* contiene un indirizzo di un buffer contenente il nome dell'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6abcd-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="6abcd-124">Questo algoritmo deve essere supportato dal driver di dispositivo e deve essere compatibile con il descrittore audio, ancora o video usato.</span><span class="sxs-lookup"><span data-stu-id="6abcd-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="6abcd-125">Se questo flag viene omesso, viene utilizzato l'algoritmo corrente.</span><span class="sxs-lookup"><span data-stu-id="6abcd-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_finestra di \_ dialogo qualità MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-127">Il driver di dispositivo dovrebbe visualizzare una finestra di dialogo per specificare il livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="6abcd-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="6abcd-128">Nella finestra di dialogo sono presenti campi specifici dell'algoritmo usati internamente dal driver di dispositivo per creare una struttura che descrive un livello di qualità specifico.</span><span class="sxs-lookup"><span data-stu-id="6abcd-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_handle di qualità MCI \_</span><span class="sxs-lookup"><span data-stu-id="6abcd-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-130">Il membro **dwHandle** della struttura identificata da *lpQuality* contiene un handle per una struttura.</span><span class="sxs-lookup"><span data-stu-id="6abcd-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="6abcd-131">La struttura contiene dati specifici dell'algoritmo che descrivono il livello di qualità specifico.</span><span class="sxs-lookup"><span data-stu-id="6abcd-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="6abcd-132">Il formato delle strutture per gli algoritmi è dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6abcd-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_elemento qualità \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-134">Una costante che indica il tipo di algoritmo è inclusa nel membro **dwItem** della struttura identificata da *lpQuality*.</span><span class="sxs-lookup"><span data-stu-id="6abcd-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="6abcd-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nome qualità \_ MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="6abcd-136">Il membro **lpstrName** della struttura identificata da *lpQuality* contiene un indirizzo di un buffer contenente il descrittore di qualità.</span><span class="sxs-lookup"><span data-stu-id="6abcd-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6abcd-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6abcd-137">Requirements</span></span>



| <span data-ttu-id="6abcd-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abcd-138">Requirement</span></span> | <span data-ttu-id="6abcd-139">Valore</span><span class="sxs-lookup"><span data-stu-id="6abcd-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6abcd-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6abcd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6abcd-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6abcd-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6abcd-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6abcd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6abcd-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6abcd-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6abcd-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6abcd-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6abcd-145"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6abcd-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abcd-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6abcd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abcd-147">MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6abcd-148">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="6abcd-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

