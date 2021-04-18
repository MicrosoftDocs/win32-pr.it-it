---
description: Consente al motore di acquisizione di utilizzare un decodificatore con restrizioni per il campo di utilizzo.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Attributo MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309585"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="1d498-103">\_Attributo di \_ sblocco \_ dell' \_ \_ attributo di \_ sblocco \_ FIELDOFUSE del motore di acquisizione MF</span><span class="sxs-lookup"><span data-stu-id="1d498-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="1d498-104">Consente al motore di acquisizione di utilizzare un decodificatore con restrizioni per il campo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="1d498-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d498-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1d498-105">Data type</span></span>

<span data-ttu-id="1d498-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="1d498-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="1d498-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d498-107">Remarks</span></span>

<span data-ttu-id="1d498-108">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="1d498-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="1d498-109">L'implementazione del chiamante di questa interfaccia è prevista per eseguire un handshake con il decodificatore, come descritto in [campo delle restrizioni di utilizzo](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1d498-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="1d498-110">Microsoft Media Foundation non definisce l'handshake, in genere comporta una sorta di scambio crittografico.</span><span class="sxs-lookup"><span data-stu-id="1d498-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="1d498-111">Internamente, il motore di acquisizione imposta il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sul decodificatore impostando l'attributo di [sblocco dell' \_ \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="1d498-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d498-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d498-112">Requirements</span></span>



| <span data-ttu-id="1d498-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d498-113">Requirement</span></span> | <span data-ttu-id="1d498-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1d498-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d498-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d498-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1d498-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1d498-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1d498-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d498-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1d498-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1d498-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1d498-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d498-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d498-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d498-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d498-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d498-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d498-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d498-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d498-123">Attributi del motore di acquisizione</span><span class="sxs-lookup"><span data-stu-id="1d498-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d498-124">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1d498-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




