---
description: Specifica il &\# 0034; bucket a perdita&\# 0034; parametri per un flusso in un sink multimediale ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Proprietà MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879598"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="5b737-103">MFPKEY \_ ASFSTREAMSINK- \_ correzione della \_ Proprietà LEAKYBUCKET</span><span class="sxs-lookup"><span data-stu-id="5b737-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="5b737-104">Specifica i parametri "leaky bucket" (vedere le note) per un flusso in un sink multimediale ASF.</span><span class="sxs-lookup"><span data-stu-id="5b737-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="5b737-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5b737-105">Data type</span></span>

<span data-ttu-id="5b737-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5b737-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5b737-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5b737-107">PROPVARIANT member</span></span>

<span data-ttu-id="5b737-108">Matrice di valori **DWORD** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="5b737-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="5b737-109">VT \_ vettore \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="5b737-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="5b737-110">**CAUL**</span><span class="sxs-lookup"><span data-stu-id="5b737-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="5b737-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b737-111">Remarks</span></span>

<span data-ttu-id="5b737-112">Un'applicazione può impostare questa proprietà su un flusso del sink multimediale ASF dopo che è stato negoziato il tipo di supporto per il flusso.</span><span class="sxs-lookup"><span data-stu-id="5b737-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="5b737-113">Utilizzare questa proprietà per specificare la finestra del buffer effettiva che verrà utilizzata dal codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5b737-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="5b737-114">È possibile ottenere queste informazioni dal codec usando l'interfaccia **IWMCodecLeakyBucket** , documentata in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5b737-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="5b737-115">Il valore di questa proprietà è una matrice di tre valori **DWORD** nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="5b737-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="5b737-116">Velocità in bit, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5b737-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="5b737-117">Dimensioni del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="5b737-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="5b737-118">Completezza del buffer iniziale, in byte.</span><span class="sxs-lookup"><span data-stu-id="5b737-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b737-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b737-119">Requirements</span></span>



| <span data-ttu-id="5b737-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b737-120">Requirement</span></span> | <span data-ttu-id="5b737-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5b737-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b737-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b737-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b737-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b737-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b737-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b737-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b737-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b737-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b737-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b737-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b737-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b737-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b737-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b737-129">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="5b737-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="5b737-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b737-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




