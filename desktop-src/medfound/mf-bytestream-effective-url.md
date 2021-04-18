---
description: Ottiene l'URL effettivo di un flusso di byte.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Attributo MF_BYTESTREAM_EFFECTIVE_URL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307982"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="3bdec-103">\_ \_ Attributo URL effettivo MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="3bdec-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="3bdec-104">Ottiene l'URL effettivo di un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="3bdec-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3bdec-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3bdec-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="3bdec-106">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="3bdec-106">Get/set</span></span>

<span data-ttu-id="3bdec-107">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="3bdec-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="3bdec-108">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="3bdec-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3bdec-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3bdec-109">Applies to</span></span>

[<span data-ttu-id="3bdec-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="3bdec-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="3bdec-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bdec-111">Remarks</span></span>

<span data-ttu-id="3bdec-112">L'URL effettivo può essere diverso dall'URL originale se l'URL originale contiene informazioni aggiuntive, ad esempio stringhe di ricerca o ancoraggi, oppure se la richiesta è stata reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="3bdec-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bdec-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bdec-113">Requirements</span></span>



| <span data-ttu-id="3bdec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bdec-114">Requirement</span></span> | <span data-ttu-id="3bdec-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3bdec-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bdec-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3bdec-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3bdec-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="3bdec-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3bdec-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3bdec-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="3bdec-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bdec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bdec-121"><dt>Mfobjects. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bdec-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bdec-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bdec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdec-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3bdec-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3bdec-124">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="3bdec-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="3bdec-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="3bdec-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




