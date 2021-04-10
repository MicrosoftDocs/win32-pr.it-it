---
title: Struttura MCI_WAVE_SET_PARMS (Mciapi. h)
description: La \_ struttura parametri di MCI WAVE \_ set \_ contiene informazioni per il \_ comando set di MCI per i dispositivi Waveform-Audio.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Struttura MCI_WAVE_SET_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874454"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="ae850-104">\_ \_ Struttura parametri set Wave MCI \_</span><span class="sxs-lookup"><span data-stu-id="ae850-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="ae850-105">La struttura **parametri di MCI \_ Wave \_ set \_** contiene informazioni per il comando [**\_ set di MCI**](mci-set.md) per i dispositivi Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="ae850-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae850-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae850-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="ae850-107">Members</span><span class="sxs-lookup"><span data-stu-id="ae850-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae850-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ae850-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="ae850-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ae850-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-111">Formato dell'ora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae850-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="ae850-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-113">Numero di canale per l'output audio.</span><span class="sxs-lookup"><span data-stu-id="ae850-113">Channel number for audio output.</span></span> <span data-ttu-id="ae850-114">Usato in genere quando si attiva o disattiva un canale.</span><span class="sxs-lookup"><span data-stu-id="ae850-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-115">**wInput**</span><span class="sxs-lookup"><span data-stu-id="ae850-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-116">Canale di input audio.</span><span class="sxs-lookup"><span data-stu-id="ae850-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-117">**wOutput**</span><span class="sxs-lookup"><span data-stu-id="ae850-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-118">Dispositivo di output da usare.</span><span class="sxs-lookup"><span data-stu-id="ae850-118">Output device to use.</span></span> <span data-ttu-id="ae850-119">Questo valore, ad esempio, può essere 2 Se un sistema ha due schede audio installate.</span><span class="sxs-lookup"><span data-stu-id="ae850-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-120">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="ae850-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-121">Formato dei dati audio della forma d'onda, come il \_ formato Wave \_ PCM.</span><span class="sxs-lookup"><span data-stu-id="ae850-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="ae850-122">I valori possibili sono definiti in mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="ae850-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="ae850-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-124">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ae850-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-125">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="ae850-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-126">Mono (1) o stereo (2).</span><span class="sxs-lookup"><span data-stu-id="ae850-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="ae850-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="ae850-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ae850-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-129">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="ae850-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-130">Campioni al secondo.</span><span class="sxs-lookup"><span data-stu-id="ae850-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-131">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="ae850-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-132">Frequenza di campionamento in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="ae850-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="ae850-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-134">Blocca l'allineamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="ae850-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="ae850-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-136">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ae850-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-137">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="ae850-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-138">BITS per campione.</span><span class="sxs-lookup"><span data-stu-id="ae850-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="ae850-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="ae850-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="ae850-140">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ae850-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae850-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae850-141">Remarks</span></span>

<span data-ttu-id="ae850-142">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="ae850-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae850-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae850-143">Requirements</span></span>



| <span data-ttu-id="ae850-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae850-144">Requirement</span></span> | <span data-ttu-id="ae850-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ae850-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ae850-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae850-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ae850-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae850-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ae850-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae850-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ae850-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae850-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ae850-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae850-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae850-151"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae850-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae850-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae850-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae850-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ae850-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ae850-154">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="ae850-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ae850-155">**SET di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ae850-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="ae850-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae850-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

