---
description: Indica quale output è l'output primario in un nodo tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Attributo MF_TOPONODE_PRIMARYOUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344166"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="f55e2-103">\_Attributo MF TOPONODE \_ PrimaryOutput poiché provocherebbe</span><span class="sxs-lookup"><span data-stu-id="f55e2-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="f55e2-104">Indica quale output è l'output primario in un nodo tee.</span><span class="sxs-lookup"><span data-stu-id="f55e2-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="f55e2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f55e2-105">Data type</span></span>

<span data-ttu-id="f55e2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f55e2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f55e2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f55e2-107">Remarks</span></span>

<span data-ttu-id="f55e2-108">Questo attributo si applica ai nodi Tee **( \_ \_ \_ nodo Tee topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="f55e2-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="f55e2-109">Il valore di questo attributo è l'indice in base zero di una connessione di output in questo nodo tee.</span><span class="sxs-lookup"><span data-stu-id="f55e2-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="f55e2-110">Questo valore indica quale output è il flusso di output primario.</span><span class="sxs-lookup"><span data-stu-id="f55e2-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="f55e2-111">La pipeline attende una richiesta dall'output primario prima di elaborare le richieste dagli altri output.</span><span class="sxs-lookup"><span data-stu-id="f55e2-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="f55e2-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f55e2-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55e2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f55e2-113">Requirements</span></span>



| <span data-ttu-id="f55e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f55e2-114">Requirement</span></span> | <span data-ttu-id="f55e2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f55e2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f55e2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f55e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f55e2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f55e2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f55e2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f55e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f55e2-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f55e2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f55e2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f55e2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55e2-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55e2-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f55e2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f55e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55e2-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f55e2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f55e2-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f55e2-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f55e2-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f55e2-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f55e2-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f55e2-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f55e2-127">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="f55e2-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




