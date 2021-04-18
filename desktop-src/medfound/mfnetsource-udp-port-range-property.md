---
description: Intervallo di porte UDP valide che l'origine di rete può usare per ricevere contenuti in streaming.
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: Proprietà MFNETSOURCE_UDP_PORT_RANGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307956"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="dc63b-103">MFNETSOURCE \_ \_ \_ Proprietà intervallo porte UDP</span><span class="sxs-lookup"><span data-stu-id="dc63b-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="dc63b-104">Intervallo di porte UDP valide che l'origine di rete può usare per ricevere contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="dc63b-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="dc63b-105">Il valore di questa proprietà è una stringa nel formato " *m*–*n* " dove *m* e *n* sono numeri di porta.</span><span class="sxs-lookup"><span data-stu-id="dc63b-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="dc63b-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="dc63b-106">Data type</span></span>

<span data-ttu-id="dc63b-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="dc63b-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="dc63b-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="dc63b-108">PROPVARIANT member</span></span>

<span data-ttu-id="dc63b-109">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="dc63b-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="dc63b-110">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="dc63b-110">VT\_LPWSTR</span></span>

<span data-ttu-id="dc63b-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="dc63b-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="dc63b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc63b-112">Remarks</span></span>

<span data-ttu-id="dc63b-113">L' **intervallo di \_ \_ porte UDP \_ MFNETSOURCE** costante definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc63b-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="dc63b-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="dc63b-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="dc63b-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="dc63b-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="dc63b-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="dc63b-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="dc63b-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="dc63b-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc63b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc63b-118">Requirements</span></span>



| <span data-ttu-id="dc63b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc63b-119">Requirement</span></span> | <span data-ttu-id="dc63b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dc63b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc63b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc63b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc63b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc63b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc63b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc63b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc63b-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc63b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc63b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc63b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc63b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc63b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc63b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc63b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc63b-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc63b-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dc63b-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc63b-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




