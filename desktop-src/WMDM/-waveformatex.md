---
title: Struttura _WAVEFORMATEX
description: La struttura \_WAVEFORMATEX definisce il formato dei dati audio della forma d’onda
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Struttura di _WAVEFORMATEX Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326482"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="202c0-104">\_Struttura WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="202c0-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="202c0-105">La struttura **\_ WAVEFORMATEX** definisce il formato dei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="202c0-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="202c0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="202c0-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="202c0-107">Members</span><span class="sxs-lookup"><span data-stu-id="202c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="202c0-108">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="202c0-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-109">Deve essere impostato su un formato o su formati supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202c0-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="202c0-110">Si noti che le versioni precedenti di Windows Media Gestione dispositivi consigliate con WMDM \_ Wave \_ Format \_ all per indicare il supporto per tutti i formati.</span><span class="sxs-lookup"><span data-stu-id="202c0-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="202c0-111">Tuttavia, questa operazione non è più consigliata, in quanto i diversi lettori multimediali interpreteranno questa operazione in modi diversi e alcuni dispositivi potranno effettivamente riprodurre qualsiasi formato di file.</span><span class="sxs-lookup"><span data-stu-id="202c0-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="202c0-112">È ora consigliabile usare WMDM \_ enum prop Valid values \_ \_ \_ \_ qualsiasi valore dell'enumerazione [**WMDM \_ enum \_ prop \_ valid \_ Values \_ form**](wmdm-enum-prop-valid-values-form.md) , oppure è opportuno specificare un intervallo di formati con la struttura [**WMDM \_ prop \_ Values \_ Range**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="202c0-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="202c0-113">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="202c0-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-114">Numero di canali nei dati audio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="202c0-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="202c0-115">I dati mono utilizzano un solo canale e i dati stereo utilizzano due canali.</span><span class="sxs-lookup"><span data-stu-id="202c0-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="202c0-116">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="202c0-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-117">Frequenza di campionamento, in campioni al secondo (hertz), in cui ogni canale deve essere riprodotto o registrato.</span><span class="sxs-lookup"><span data-stu-id="202c0-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="202c0-118">I valori comuni per **nSamplesPerSec** sono 8,0 kilohertz (kHz), 11,025 khz, 22,05 khz e 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="202c0-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="202c0-119">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="202c0-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-120">Velocità di trasferimento dati media necessaria per il tag di formato, in byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="202c0-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="202c0-121">Per la riproduzione e la registrazione del software è possibile stimare le dimensioni del buffer usando il membro **nAvgBytesPerSec** .</span><span class="sxs-lookup"><span data-stu-id="202c0-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="202c0-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="202c0-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-123">Allineamento del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="202c0-123">Block alignment, in bytes.</span></span> <span data-ttu-id="202c0-124">L'allineamento del blocco è l'unità atomica minima dei dati per il tipo di formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="202c0-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="202c0-125">La riproduzione e la registrazione del software devono elaborare un multiplo di byte di **nBlockAlign** di dati alla volta.</span><span class="sxs-lookup"><span data-stu-id="202c0-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="202c0-126">I dati scritti e letti da un dispositivo devono sempre iniziare all'inizio di un blocco.</span><span class="sxs-lookup"><span data-stu-id="202c0-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="202c0-127">Non è ad esempio possibile avviare correttamente la riproduzione dei dati PCM al centro di un campione (ovvero su un limite non allineato a blocchi).</span><span class="sxs-lookup"><span data-stu-id="202c0-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="202c0-128">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="202c0-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-129">Bit per campione per il tipo di formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="202c0-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="202c0-130">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="202c0-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="202c0-131">Questo membro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="202c0-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="202c0-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="202c0-132">Requirements</span></span>



| <span data-ttu-id="202c0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="202c0-133">Requirement</span></span> | <span data-ttu-id="202c0-134">Valore</span><span class="sxs-lookup"><span data-stu-id="202c0-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="202c0-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="202c0-135">Header</span></span><br/> | <dl> <span data-ttu-id="202c0-136"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="202c0-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202c0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="202c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202c0-138">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="202c0-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="202c0-139">**IMDSPStorage:: CreateStorage**</span><span class="sxs-lookup"><span data-stu-id="202c0-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="202c0-140">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="202c0-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="202c0-141">**IWMDMDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="202c0-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="202c0-142">**IWMDMOperation::GetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="202c0-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="202c0-143">**IWMDMOperation::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="202c0-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="202c0-144">**IWMDMStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="202c0-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="202c0-145">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="202c0-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





