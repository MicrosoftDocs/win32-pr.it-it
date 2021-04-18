---
description: Specifica se è abilitato il trasporto RTSP (Real-Time Streaming Protocol) nell'origine di rete.
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: Proprietà MFNETSOURCE_ENABLE_RTSP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308401"
---
# <a name="mfnetsource_enable_rtsp-property"></a><span data-ttu-id="d0aba-103">MFNETSOURCE \_ Abilita la \_ Proprietà RTSP</span><span class="sxs-lookup"><span data-stu-id="d0aba-103">MFNETSOURCE\_ENABLE\_RTSP property</span></span>

<span data-ttu-id="d0aba-104">Specifica se è abilitato il trasporto RTSP (Real-Time Streaming Protocol) nell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="d0aba-104">Specifies whether Real-Time Streaming Protocol (RTSP) transport is enabled in the network source.</span></span>



<span data-ttu-id="d0aba-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d0aba-105">Data type</span></span>

<span data-ttu-id="d0aba-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d0aba-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d0aba-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d0aba-107">PROPVARIANT member</span></span>

<span data-ttu-id="d0aba-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="d0aba-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="d0aba-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d0aba-109">VT\_I4</span></span>

<span data-ttu-id="d0aba-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d0aba-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d0aba-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0aba-111">Remarks</span></span>

<span data-ttu-id="d0aba-112">La costante **MFNETSOURCE \_ Abilita \_ RTSP** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d0aba-112">The constant **MFNETSOURCE\_ENABLE\_RTSP** defines the GUID for this property key.</span></span> <span data-ttu-id="d0aba-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="d0aba-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d0aba-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="d0aba-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d0aba-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="d0aba-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d0aba-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0aba-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0aba-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0aba-117">Requirements</span></span>



| <span data-ttu-id="d0aba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0aba-118">Requirement</span></span> | <span data-ttu-id="d0aba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d0aba-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0aba-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0aba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0aba-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0aba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0aba-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0aba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0aba-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0aba-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d0aba-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0aba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0aba-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0aba-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0aba-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0aba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0aba-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0aba-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d0aba-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0aba-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d0aba-129">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="d0aba-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




