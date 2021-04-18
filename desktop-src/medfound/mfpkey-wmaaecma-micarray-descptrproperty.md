---
description: Specifica la geometria della matrice di microfoni per il DSP di acquisizione voce.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Proprietà MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309117"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="c7acf-103">MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR proprietà</span><span class="sxs-lookup"><span data-stu-id="c7acf-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="c7acf-104">Specifica la geometria della matrice di microfoni per il DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="c7acf-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c7acf-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c7acf-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c7acf-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c7acf-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c7acf-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c7acf-107">Data Type</span></span>

<span data-ttu-id="c7acf-108">\_BLOB VT</span><span class="sxs-lookup"><span data-stu-id="c7acf-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="c7acf-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c7acf-109">Applies To</span></span>

-   [<span data-ttu-id="c7acf-110">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="c7acf-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c7acf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7acf-111">Remarks</span></span>

<span data-ttu-id="c7acf-112">Il valore di questa proprietà è una [**struttura \_ \_ \_ Geometry della matrice KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) .</span><span class="sxs-lookup"><span data-stu-id="c7acf-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="c7acf-113">Questa struttura viene definita nel file di intestazione KsMedia. h.</span><span class="sxs-lookup"><span data-stu-id="c7acf-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="c7acf-114">Per ottenere la geometria della matrice di microfoni, eseguire una query sul dispositivo audio per la \_ \_ Proprietà Geometry della matrice KSPROPERTY audio mic chiamando \_ \_ il metodo **IKsControl:: KSPROPERTY** sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7acf-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="c7acf-115">Per ulteriori informazioni sugli array di microfoni, scaricare il white paper [come compilare e utilizzare gli array di microfoni per Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="c7acf-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="c7acf-116">Impostare questa proprietà se si utilizza il DSP in modalità filtro ed è abilitata l'elaborazione di matrici di microfoni.</span><span class="sxs-lookup"><span data-stu-id="c7acf-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="c7acf-117">Se si usa il DSP in modalità origine, il DSP esegue automaticamente una query sul dispositivo per le informazioni di geometria.</span><span class="sxs-lookup"><span data-stu-id="c7acf-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7acf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7acf-118">Requirements</span></span>



| <span data-ttu-id="c7acf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7acf-119">Requirement</span></span> | <span data-ttu-id="c7acf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c7acf-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7acf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7acf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7acf-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7acf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7acf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7acf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7acf-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7acf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7acf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7acf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7acf-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7acf-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7acf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7acf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7acf-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7acf-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c7acf-129">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="c7acf-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
