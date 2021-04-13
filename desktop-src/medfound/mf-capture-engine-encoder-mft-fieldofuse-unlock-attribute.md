---
description: Consente al motore di acquisizione di usare un codificatore con restrizioni di campo per l'utilizzo.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Attributo MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226650"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="c5f17-103">\_Attributo dell' \_ \_ \_ \_ \_ \_ attributo Unlock del codificatore MFT FIELDOFUSE di MF Capture Engine</span><span class="sxs-lookup"><span data-stu-id="c5f17-103">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="c5f17-104">Consente al motore di acquisizione di usare un codificatore con restrizioni di campo per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c5f17-104">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5f17-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c5f17-105">Data type</span></span>

<span data-ttu-id="c5f17-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="c5f17-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f17-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5f17-107">Remarks</span></span>

<span data-ttu-id="c5f17-108">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="c5f17-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="c5f17-109">L'implementazione del chiamante di questa interfaccia è prevista per l'esecuzione di un handshake con il codificatore, come descritto in [campo delle restrizioni di utilizzo](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c5f17-109">The caller's implementation of this interface is expected to perform a handshake with the encoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="c5f17-110">Microsoft Media Foundation non definisce l'handshake, in genere comporta una sorta di scambio crittografico.</span><span class="sxs-lookup"><span data-stu-id="c5f17-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="c5f17-111">Internamente, il motore di acquisizione imposta il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sul codificatore impostando l'attributo di [sblocco dell' \_ \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c5f17-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the encoder by setting the encoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f17-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5f17-112">Requirements</span></span>



| <span data-ttu-id="c5f17-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f17-113">Requirement</span></span> | <span data-ttu-id="c5f17-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c5f17-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f17-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5f17-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f17-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5f17-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c5f17-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5f17-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f17-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5f17-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5f17-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5f17-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5f17-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f17-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f17-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5f17-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f17-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5f17-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5f17-123">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="c5f17-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5f17-124">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="c5f17-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




