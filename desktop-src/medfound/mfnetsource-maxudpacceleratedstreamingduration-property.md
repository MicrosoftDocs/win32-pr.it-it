---
description: Durata massima del flusso accelerato, in millisecondi, quando l'origine di rete utilizza il trasporto UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Proprietà MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058209"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="925cd-103">\_Proprietà MAXUDPACCELERATEDSTREAMINGDURATION di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="925cd-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="925cd-104">Durata massima del flusso accelerato, in millisecondi, quando l'origine di rete utilizza il trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="925cd-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="925cd-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="925cd-105">Data type</span></span>

<span data-ttu-id="925cd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="925cd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="925cd-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="925cd-107">PROPVARIANT member</span></span>

<span data-ttu-id="925cd-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="925cd-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="925cd-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="925cd-109">VT\_I4</span></span>

<span data-ttu-id="925cd-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="925cd-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="925cd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="925cd-111">Remarks</span></span>

<span data-ttu-id="925cd-112">La costante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="925cd-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="925cd-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="925cd-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="925cd-114">Per il trasporto UDP, questa proprietà esegue l'override della proprietà [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) se il valore di questa proprietà è inferiore.</span><span class="sxs-lookup"><span data-stu-id="925cd-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="925cd-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="925cd-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="925cd-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="925cd-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="925cd-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="925cd-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="925cd-118">Il valore predefinito di questa proprietà è 8.000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="925cd-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="925cd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="925cd-119">Requirements</span></span>



| <span data-ttu-id="925cd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="925cd-120">Requirement</span></span> | <span data-ttu-id="925cd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="925cd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="925cd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="925cd-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="925cd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="925cd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="925cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="925cd-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="925cd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="925cd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="925cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="925cd-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="925cd-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="925cd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="925cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925cd-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="925cd-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="925cd-130">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="925cd-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="925cd-131">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="925cd-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




