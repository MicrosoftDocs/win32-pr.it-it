---
description: Specifica la larghezza di banda della coppia di pacchetti e la larghezza di banda della fase di esecuzione rilevata dall'origine di rete.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Proprietà MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309533"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="a80c8-103">\_Proprietà PPBANDWIDTH di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="a80c8-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="a80c8-104">Specifica la larghezza di banda della coppia di pacchetti e la larghezza di banda della fase di esecuzione rilevata dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="a80c8-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="a80c8-105">Il valore della proprietà è una matrice di due valori:</span><span class="sxs-lookup"><span data-stu-id="a80c8-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="a80c8-106">Larghezza di banda di coppie di pacchetti, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a80c8-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="a80c8-107">Larghezza di banda della fase di esecuzione, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a80c8-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="a80c8-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a80c8-108">Data type</span></span>

<span data-ttu-id="a80c8-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a80c8-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a80c8-110">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a80c8-110">PROPVARIANT member</span></span>

<span data-ttu-id="a80c8-111">Matrice di valori **ULONG** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="a80c8-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="a80c8-112">VT \_ vettore \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="a80c8-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="a80c8-113">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="a80c8-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="a80c8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a80c8-114">Remarks</span></span>

<span data-ttu-id="a80c8-115">La costante **MFNETSOURCE \_ PPBANDWIDTH** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a80c8-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="a80c8-116">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="a80c8-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a80c8-117">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a80c8-117">This property is read-only.</span></span> <span data-ttu-id="a80c8-118">Per recuperare questa proprietà, eseguire una query sull'origine di rete per l'interfaccia **IPropertyStore** e chiamare **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="a80c8-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80c8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a80c8-119">Requirements</span></span>



| <span data-ttu-id="a80c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80c8-120">Requirement</span></span> | <span data-ttu-id="a80c8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a80c8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a80c8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a80c8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a80c8-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a80c8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a80c8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a80c8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a80c8-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a80c8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a80c8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a80c8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80c8-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80c8-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80c8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a80c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80c8-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a80c8-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a80c8-130">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="a80c8-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="a80c8-131">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a80c8-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




