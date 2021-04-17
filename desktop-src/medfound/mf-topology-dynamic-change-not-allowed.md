---
description: Specifica se la sessione multimediale tenta di modificare la topologia quando il formato di un flusso viene modificato.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Attributo MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484804"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="0d7f6-103">Attributo per la \_ modifica dinamica della topologia MF \_ \_ \_ non \_ consentito</span><span class="sxs-lookup"><span data-stu-id="0d7f6-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="0d7f6-104">Specifica se la sessione multimediale tenta di modificare la topologia quando il formato di un flusso viene modificato.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d7f6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0d7f6-105">Data type</span></span>

<span data-ttu-id="0d7f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d7f6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0d7f6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="0d7f6-107">Get/set</span></span>

<span data-ttu-id="0d7f6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0d7f6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0d7f6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0d7f6-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="0d7f6-110">Applies to</span></span>

[<span data-ttu-id="0d7f6-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="0d7f6-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="0d7f6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d7f6-112">Remarks</span></span>

<span data-ttu-id="0d7f6-113">Questo attributo controlla il modo in cui la sessione multimediale risponde se il formato di un flusso cambia durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="0d7f6-114">Se il formato viene modificato e l' \_ attributo della modifica dinamica della topologia MF \_ \_ \_ non \_ è consentito è **false**, la sessione multimediale potrebbe inserire nuovi nodi nella topologia in modo che corrispondano al nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="0d7f6-115">Se, ad esempio, le dimensioni del video cambiano, la sessione multimediale potrebbe aggiungere una trasformazione Media Foundation (MFT) che ridimensiona il video.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="0d7f6-116">In caso contrario, se l'attributo è **true**, la topologia non verrà modificata dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="0d7f6-117">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="0d7f6-118">Il valore consigliato è **false**.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="0d7f6-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0d7f6-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d7f6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d7f6-120">Requirements</span></span>



| <span data-ttu-id="0d7f6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d7f6-121">Requirement</span></span> | <span data-ttu-id="0d7f6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0d7f6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d7f6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7f6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d7f6-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d7f6-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d7f6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d7f6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d7f6-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d7f6-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0d7f6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d7f6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d7f6-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d7f6-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d7f6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d7f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7f6-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d7f6-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d7f6-131">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="0d7f6-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




