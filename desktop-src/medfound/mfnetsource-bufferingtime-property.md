---
description: Numero di secondi di dati che l'origine di rete memorizza nel buffer all'avvio.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: Proprietà MFNETSOURCE_BUFFERINGTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130119"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="f24e0-103">\_Proprietà BUFFERINGTIME di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="f24e0-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="f24e0-104">Numero di secondi di dati che l'origine di rete memorizza nel buffer all'avvio.</span><span class="sxs-lookup"><span data-stu-id="f24e0-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="f24e0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f24e0-105">Data type</span></span>

<span data-ttu-id="f24e0-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f24e0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f24e0-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f24e0-107">PROPVARIANT member</span></span>

<span data-ttu-id="f24e0-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="f24e0-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="f24e0-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f24e0-109">VT\_I4</span></span>

<span data-ttu-id="f24e0-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f24e0-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f24e0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f24e0-111">Remarks</span></span>

<span data-ttu-id="f24e0-112">La costante **MFNETSOURCE \_ BUFFERINGTIME** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f24e0-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="f24e0-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="f24e0-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f24e0-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="f24e0-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="f24e0-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="f24e0-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f24e0-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f24e0-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="f24e0-117">Il valore predefinito di questa proprietà è 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="f24e0-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f24e0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f24e0-118">Requirements</span></span>



| <span data-ttu-id="f24e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f24e0-119">Requirement</span></span> | <span data-ttu-id="f24e0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f24e0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f24e0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f24e0-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f24e0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f24e0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f24e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f24e0-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f24e0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f24e0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f24e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f24e0-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24e0-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24e0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f24e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24e0-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f24e0-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f24e0-129">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="f24e0-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="f24e0-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f24e0-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




