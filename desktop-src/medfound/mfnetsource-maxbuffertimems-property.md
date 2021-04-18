---
description: Quantità massima di dati memorizzati nei buffer di origine della rete, in millisecondi.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Proprietà MFNETSOURCE_MAXBUFFERTIMEMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307961"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="360d9-103">\_Proprietà MAXBUFFERTIMEMS di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="360d9-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="360d9-104">Quantità massima di dati memorizzati nei buffer di origine della rete, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="360d9-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="360d9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="360d9-105">Data type</span></span>

<span data-ttu-id="360d9-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="360d9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="360d9-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="360d9-107">PROPVARIANT member</span></span>

<span data-ttu-id="360d9-108">**DWORD** (archiviato come **Long**)</span><span class="sxs-lookup"><span data-stu-id="360d9-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="360d9-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="360d9-109">VT\_I4</span></span>

<span data-ttu-id="360d9-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="360d9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="360d9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="360d9-111">Remarks</span></span>

<span data-ttu-id="360d9-112">La costante **MFNETSOURCE \_ MAXBUFFERTIMEMS** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="360d9-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="360d9-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="360d9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="360d9-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="360d9-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="360d9-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="360d9-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="360d9-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="360d9-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="360d9-117">Il valore predefinito di questa proprietà è 40.000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="360d9-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="360d9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="360d9-118">Requirements</span></span>



| <span data-ttu-id="360d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="360d9-119">Requirement</span></span> | <span data-ttu-id="360d9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="360d9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="360d9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="360d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="360d9-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="360d9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="360d9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="360d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="360d9-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="360d9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="360d9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="360d9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="360d9-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="360d9-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="360d9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="360d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360d9-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="360d9-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="360d9-129">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="360d9-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="360d9-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="360d9-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




