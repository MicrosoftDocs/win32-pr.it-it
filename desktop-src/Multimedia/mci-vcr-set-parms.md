---
title: Struttura MCI_VCR_SET_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ set contiene i \_ parametri per il \_ comando set MCI per i registratori di nastri video.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Struttura MCI_VCR_SET_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400864"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="6fa12-104">\_ \_ Struttura parametri set VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="6fa12-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="6fa12-105">La struttura **parametri di MCI \_ VCR \_ set \_** contiene i parametri per il comando [**\_ set MCI**](mci-set.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="6fa12-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa12-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fa12-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="6fa12-107">Members</span><span class="sxs-lookup"><span data-stu-id="6fa12-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fa12-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6fa12-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="6fa12-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6fa12-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-111">Formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="6fa12-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="6fa12-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6fa12-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-114">**dwTimeMode**</span><span class="sxs-lookup"><span data-stu-id="6fa12-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-115">Costante che specifica l'origine dell'intervallo utilizzata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fa12-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="6fa12-116">L'origine dell'intervallo è un timecode registrato in un nastro o i contatori nel dispositivo che rilevano lo spostamento del nastro.</span><span class="sxs-lookup"><span data-stu-id="6fa12-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-117">**dwRecordFormat**</span><span class="sxs-lookup"><span data-stu-id="6fa12-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-118">Velocità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="6fa12-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-119">**dwCounterFormat**</span><span class="sxs-lookup"><span data-stu-id="6fa12-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-120">Formato di un nuovo valore di ora del contatore.</span><span class="sxs-lookup"><span data-stu-id="6fa12-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="6fa12-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-122">Contenuto della visualizzazione sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="6fa12-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-123">**dwTracking**</span><span class="sxs-lookup"><span data-stu-id="6fa12-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-124">Regolazione della velocità utilizzata per tenere traccia della frequenza di riproduzione dei VCR.</span><span class="sxs-lookup"><span data-stu-id="6fa12-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-125">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="6fa12-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-126">Velocità di riproduzione usata dal dispositivo come numero intero.</span><span class="sxs-lookup"><span data-stu-id="6fa12-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="6fa12-127">La velocità di riproduzione normale è 1000, la velocità doppia è 2000 e la metà della velocità è 500.</span><span class="sxs-lookup"><span data-stu-id="6fa12-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="6fa12-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-129">Lunghezza del nastro quando la lunghezza non è rilevabile dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fa12-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-130">**dwCounter**</span><span class="sxs-lookup"><span data-stu-id="6fa12-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-131">Nuovo valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="6fa12-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-132">**dwClock**</span><span class="sxs-lookup"><span data-stu-id="6fa12-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-133">Nuova ora di clock.</span><span class="sxs-lookup"><span data-stu-id="6fa12-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-134">**dwPauseTimeout**</span><span class="sxs-lookup"><span data-stu-id="6fa12-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-135">Nuovo valore di timeout per il comando Sospendi.</span><span class="sxs-lookup"><span data-stu-id="6fa12-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-136">**dwPrerollDuration**</span><span class="sxs-lookup"><span data-stu-id="6fa12-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-137">Lunghezza del nastro necessaria per stabilizzare l'output del VCR.</span><span class="sxs-lookup"><span data-stu-id="6fa12-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="6fa12-138">**dwPostrollDuration**</span><span class="sxs-lookup"><span data-stu-id="6fa12-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="6fa12-139">Lunghezza del nastro necessaria per bloccare il trasporto VCR quando viene emesso un comando [**MCI \_ Stop**](mci-stop.md) o [**MCI \_ pause**](mci-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa12-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fa12-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fa12-140">Remarks</span></span>

<span data-ttu-id="6fa12-141">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="6fa12-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa12-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fa12-142">Requirements</span></span>



| <span data-ttu-id="6fa12-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa12-143">Requirement</span></span> | <span data-ttu-id="6fa12-144">Valore</span><span class="sxs-lookup"><span data-stu-id="6fa12-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6fa12-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa12-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa12-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6fa12-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6fa12-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa12-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa12-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6fa12-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6fa12-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fa12-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa12-150"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa12-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa12-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fa12-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa12-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6fa12-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6fa12-153">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="6fa12-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6fa12-154">**\_pausa MCI**</span><span class="sxs-lookup"><span data-stu-id="6fa12-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="6fa12-155">**SET di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="6fa12-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="6fa12-156">**\_arresto MCI**</span><span class="sxs-lookup"><span data-stu-id="6fa12-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="6fa12-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fa12-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

