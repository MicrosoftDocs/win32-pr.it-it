---
description: Identificatore di flusso del sink di flusso associato a questo nodo della topologia.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: Attributo MF_TOPONODE_STREAMID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308436"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="912fa-103">\_Attributo MF TOPONODE \_ STREAMID</span><span class="sxs-lookup"><span data-stu-id="912fa-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="912fa-104">Identificatore di flusso del sink di flusso associato a questo nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="912fa-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="912fa-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="912fa-105">Data type</span></span>

<span data-ttu-id="912fa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="912fa-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="912fa-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="912fa-107">Remarks</span></span>

<span data-ttu-id="912fa-108">Questo attributo si applica ai nodi di output (**\_ nodo di \_ output \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="912fa-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="912fa-109">Quando viene caricata la topologia, la sessione multimediale esegue una query sul sink multimediale per un sink di flusso con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="912fa-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="912fa-110">Se l'operazione ha esito negativo, tenta di aggiungere un nuovo sink di flusso al sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="912fa-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="912fa-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="912fa-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="912fa-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="912fa-112">Requirements</span></span>



| <span data-ttu-id="912fa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="912fa-113">Requirement</span></span> | <span data-ttu-id="912fa-114">Valore</span><span class="sxs-lookup"><span data-stu-id="912fa-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="912fa-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="912fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="912fa-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="912fa-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="912fa-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="912fa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="912fa-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="912fa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="912fa-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="912fa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="912fa-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="912fa-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912fa-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="912fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912fa-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="912fa-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="912fa-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="912fa-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="912fa-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="912fa-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="912fa-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="912fa-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="912fa-126">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="912fa-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




