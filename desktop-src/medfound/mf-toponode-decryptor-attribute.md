---
description: Specifica se un oggetto sottostante di un nodo della topologia è una Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Attributo MF_TOPONODE_DECRYPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318048"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="b3723-103">\_Attributo di \_ decrittografia MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="b3723-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="b3723-104">Specifica se l'oggetto sottostante di un nodo della topologia è una Decrypter.</span><span class="sxs-lookup"><span data-stu-id="b3723-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3723-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b3723-105">Data type</span></span>

<span data-ttu-id="b3723-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b3723-106">**UINT32**</span></span>

<span data-ttu-id="b3723-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="b3723-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3723-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3723-108">Remarks</span></span>

<span data-ttu-id="b3723-109">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="b3723-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="b3723-110">Se il valore di questo attributo è diverso da zero, l'oggetto sottostante del nodo è un oggetto Decrypter.</span><span class="sxs-lookup"><span data-stu-id="b3723-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="b3723-111">Le applicazioni in genere non utilizzano direttamente questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b3723-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="b3723-112">La sessione multimediale imposta questo attributo quando crea un nodo per una Decrypter, ottenuta dal metodo [**IMFInputTrustAuthority:: Decryptor**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .</span><span class="sxs-lookup"><span data-stu-id="b3723-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="b3723-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b3723-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3723-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3723-114">Requirements</span></span>



| <span data-ttu-id="b3723-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3723-115">Requirement</span></span> | <span data-ttu-id="b3723-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b3723-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3723-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3723-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b3723-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3723-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3723-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3723-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b3723-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3723-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3723-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3723-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3723-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3723-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3723-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3723-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3723-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3723-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3723-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="b3723-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b3723-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="b3723-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b3723-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b3723-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b3723-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="b3723-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




