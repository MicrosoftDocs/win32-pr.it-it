---
description: Durata del flusso accelerato per l'origine di rete, in millisecondi.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Proprietà MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879810"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="e714b-103">\_Proprietà ACCELERATEDSTREAMINGDURATION di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="e714b-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="e714b-104">Durata del flusso accelerato per l'origine di rete, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="e714b-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="e714b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e714b-105">Data type</span></span>

<span data-ttu-id="e714b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e714b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e714b-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e714b-107">PROPVARIANT member</span></span>

<span data-ttu-id="e714b-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="e714b-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="e714b-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e714b-109">VT\_I4</span></span>

<span data-ttu-id="e714b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e714b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e714b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e714b-111">Remarks</span></span>

<span data-ttu-id="e714b-112">La costante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e714b-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="e714b-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="e714b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e714b-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="e714b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e714b-115">Per impostare la proprietà, passare un oggetto **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="e714b-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="e714b-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e714b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e714b-117">Questa proprietà si applica alla funzionalità di avvio rapido di servizi Windows Media, che riproduce rapidamente il contenuto senza attendere la lunga memorizzazione nella memoria iniziale.</span><span class="sxs-lookup"><span data-stu-id="e714b-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="e714b-118">Quando si utilizza avvio rapido, il server che esegue Windows Media Services invierà alcuni dati all'inizio del contenuto a una velocità più elevata rispetto a quella specificata dalla velocità in bit del contenuto.</span><span class="sxs-lookup"><span data-stu-id="e714b-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="e714b-119">Il valore predefinito di questa proprietà è 10.000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="e714b-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e714b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e714b-120">Requirements</span></span>



| <span data-ttu-id="e714b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e714b-121">Requirement</span></span> | <span data-ttu-id="e714b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e714b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e714b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e714b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e714b-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e714b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e714b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e714b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e714b-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e714b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e714b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e714b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e714b-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e714b-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e714b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e714b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e714b-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e714b-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e714b-131">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="e714b-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="e714b-132">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e714b-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




