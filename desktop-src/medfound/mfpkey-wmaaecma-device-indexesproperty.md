---
description: Specifica i dispositivi audio usati dal DSP di acquisizione vocale per l'acquisizione e il rendering dell'audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Proprietà MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880082"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="de5ab-103">\_Proprietà degli \_ indici del dispositivo WMAAECMA di MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="de5ab-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="de5ab-104">Specifica i dispositivi audio usati dal DSP di acquisizione vocale per l'acquisizione e il rendering dell'audio.</span><span class="sxs-lookup"><span data-stu-id="de5ab-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="de5ab-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="de5ab-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="de5ab-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="de5ab-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="de5ab-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="de5ab-107">Data Type</span></span>

<span data-ttu-id="de5ab-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="de5ab-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="de5ab-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="de5ab-109">Default Value</span></span>

<span data-ttu-id="de5ab-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="de5ab-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="de5ab-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="de5ab-111">Applies To</span></span>

-   [<span data-ttu-id="de5ab-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="de5ab-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="de5ab-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5ab-113">Remarks</span></span>

<span data-ttu-id="de5ab-114">Impostare questa proprietà se si utilizza il DSP in modalità origine.</span><span class="sxs-lookup"><span data-stu-id="de5ab-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="de5ab-115">Il DSP ignora questa proprietà in modalità filtro.</span><span class="sxs-lookup"><span data-stu-id="de5ab-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="de5ab-116">Il valore della proprietà è costituito da **parole** a 2 16 bit compresse in un valore **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="de5ab-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="de5ab-117">I 16 bit superiori specificano il dispositivo di rendering audio (in genere un altoparlante) e i 16 bit inferiori specificano il dispositivo di acquisizione (in genere un microfono).</span><span class="sxs-lookup"><span data-stu-id="de5ab-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="de5ab-118">Ogni dispositivo viene specificato come indice nella raccolta di dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="de5ab-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="de5ab-119">Se l'indice è-1, viene usato il dispositivo predefinito.</span><span class="sxs-lookup"><span data-stu-id="de5ab-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="de5ab-120">L'indice del dispositivo corrisponde all'indice della raccolta usato nell'interfaccia [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) .</span><span class="sxs-lookup"><span data-stu-id="de5ab-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="de5ab-121">L'applicazione deve riprodurre la voce finale tramite il dispositivo di rendering selezionato.</span><span class="sxs-lookup"><span data-stu-id="de5ab-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="de5ab-122">(La voce finale è la voce della persona sull'altra estremità della linea telefonica, che viene riprodotta attraverso l'altoparlante sul computer dell'utente). Se il dispositivo di rendering selezionato non dispone di un flusso attivo, il DSP non può elaborare alcun output.</span><span class="sxs-lookup"><span data-stu-id="de5ab-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="de5ab-123">Il valore predefinito di questa proprietà è (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="de5ab-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="de5ab-124">Nell'esempio seguente viene illustrato come inizializzare **PROPVARIANT** per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="de5ab-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="de5ab-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de5ab-125">Requirements</span></span>



| <span data-ttu-id="de5ab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5ab-126">Requirement</span></span> | <span data-ttu-id="de5ab-127">Valore</span><span class="sxs-lookup"><span data-stu-id="de5ab-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de5ab-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de5ab-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de5ab-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de5ab-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de5ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de5ab-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de5ab-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de5ab-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de5ab-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="de5ab-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de5ab-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5ab-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de5ab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5ab-135">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de5ab-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="de5ab-136">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="de5ab-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
