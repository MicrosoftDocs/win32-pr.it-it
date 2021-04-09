---
description: Contiene il codice di errore dell'errore di connessione più recente per questo nodo di topologia.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Attributo MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130143"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="ada5c-103">\_Attributo MF TOPONODE \_ ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ada5c-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="ada5c-104">Contiene il codice di errore dell'errore di connessione più recente per questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="ada5c-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="ada5c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ada5c-105">Data type</span></span>

<span data-ttu-id="ada5c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ada5c-106">**UINT32**</span></span>

<span data-ttu-id="ada5c-107">Ttreat come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ada5c-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ada5c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ada5c-108">Remarks</span></span>

<span data-ttu-id="ada5c-109">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="ada5c-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="ada5c-110">Il valore di questo attributo è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ada5c-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="ada5c-111">La sessione multimediale o il caricatore della topologia potrebbe impostare l'attributo.</span><span class="sxs-lookup"><span data-stu-id="ada5c-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="ada5c-112">Le applicazioni in genere leggono questo attributo ma non lo impostano.</span><span class="sxs-lookup"><span data-stu-id="ada5c-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="ada5c-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ada5c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada5c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ada5c-114">Requirements</span></span>



| <span data-ttu-id="ada5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada5c-115">Requirement</span></span> | <span data-ttu-id="ada5c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ada5c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ada5c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ada5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ada5c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ada5c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ada5c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ada5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ada5c-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ada5c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ada5c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ada5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ada5c-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada5c-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ada5c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ada5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada5c-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ada5c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ada5c-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ada5c-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ada5c-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ada5c-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ada5c-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="ada5c-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ada5c-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="ada5c-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




