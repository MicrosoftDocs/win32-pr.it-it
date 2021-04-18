---
description: Specifica quando una trasformazione viene scaricata.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Attributo MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308447"
---
# <a name="mf_toponode_flush-attribute"></a><span data-ttu-id="68b9d-103">\_Attributo di \_ scaricamento MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="68b9d-103">MF\_TOPONODE\_FLUSH attribute</span></span>

<span data-ttu-id="68b9d-104">Specifica quando una trasformazione viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="68b9d-104">Specifies when a transform is flushed.</span></span>

## <a name="data-type"></a><span data-ttu-id="68b9d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="68b9d-105">Data type</span></span>

<span data-ttu-id="68b9d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68b9d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="68b9d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="68b9d-107">Remarks</span></span>

<span data-ttu-id="68b9d-108">Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="68b9d-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="68b9d-109">Il valore dell'attributo è un membro dell'enumerazione della [**\_ \_ \_ modalità di scaricamento MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) .</span><span class="sxs-lookup"><span data-stu-id="68b9d-109">The value of the attribute is a member of the [**MF\_TOPONODE\_FLUSH\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) enumeration.</span></span> <span data-ttu-id="68b9d-110">Se questo attributo non è impostato, il valore predefinito è **MF \_ TOPONODE \_ Flush \_ Always**.</span><span class="sxs-lookup"><span data-stu-id="68b9d-110">If this attribute is not set, the default value is **MF\_TOPONODE\_FLUSH\_ALWAYS**.</span></span>

<span data-ttu-id="68b9d-111">Lo svuotamento viene eseguito chiamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) nella trasformazione con il messaggio di [**\_ \_ \_ scaricamento del comando del messaggio MFT**](mft-message-command-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="68b9d-111">Flushing is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="68b9d-112">Per ulteriori informazioni, vedere l'enumerazione del [**\_ \_ tipo di messaggio MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .</span><span class="sxs-lookup"><span data-stu-id="68b9d-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="68b9d-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68b9d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b9d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68b9d-114">Requirements</span></span>



| <span data-ttu-id="68b9d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b9d-115">Requirement</span></span> | <span data-ttu-id="68b9d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="68b9d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68b9d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68b9d-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68b9d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68b9d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68b9d-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68b9d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68b9d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68b9d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b9d-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b9d-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b9d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68b9d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b9d-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68b9d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68b9d-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="68b9d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68b9d-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="68b9d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68b9d-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="68b9d-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="68b9d-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="68b9d-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




