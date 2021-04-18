---
description: Attributo passato in IMFMediaEngineNeedKeyNotify al motore multimediale al momento della creazione.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Attributo MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320717"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="bdaf9-103">\_Attributo di \_ \_ callback NEEDKEY del motore multimediale MF \_</span><span class="sxs-lookup"><span data-stu-id="bdaf9-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="bdaf9-104">Attributo passato in [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) al motore multimediale al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="bdaf9-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="bdaf9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bdaf9-105">Data type</span></span>

<span data-ttu-id="bdaf9-106">**IMFMediaEngineNeedKeyNotify \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="bdaf9-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="bdaf9-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="bdaf9-107">Get/set</span></span>

<span data-ttu-id="bdaf9-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="bdaf9-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="bdaf9-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="bdaf9-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdaf9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdaf9-110">Remarks</span></span>

<span data-ttu-id="bdaf9-111">Il valore di questo attributo è un puntatore all'interfaccia [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bdaf9-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdaf9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdaf9-112">Requirements</span></span>



| <span data-ttu-id="bdaf9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdaf9-113">Requirement</span></span> | <span data-ttu-id="bdaf9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bdaf9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdaf9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdaf9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bdaf9-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdaf9-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bdaf9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdaf9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bdaf9-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdaf9-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bdaf9-119">IDL</span><span class="sxs-lookup"><span data-stu-id="bdaf9-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdaf9-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdaf9-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdaf9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdaf9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdaf9-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdaf9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




