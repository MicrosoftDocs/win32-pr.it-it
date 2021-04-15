---
description: Specifica se sono abilitati tutti i protocolli di streaming.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: Proprietà MFNETSOURCE_ENABLE_STREAMING (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527378"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="2bd72-103">\_Proprietà Abilita \_ flusso di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="2bd72-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="2bd72-104">Specifica se sono abilitati tutti i protocolli di streaming.</span><span class="sxs-lookup"><span data-stu-id="2bd72-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="2bd72-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2bd72-105">Data type</span></span>

<span data-ttu-id="2bd72-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2bd72-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2bd72-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2bd72-107">PROPVARIANT member</span></span>

<span data-ttu-id="2bd72-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="2bd72-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="2bd72-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2bd72-109">VT\_I4</span></span>

<span data-ttu-id="2bd72-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="2bd72-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2bd72-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd72-111">Remarks</span></span>

<span data-ttu-id="2bd72-112">La costante **MFNETSOURCE \_ enable \_ streaming** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2bd72-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="2bd72-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="2bd72-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="2bd72-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="2bd72-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="2bd72-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** alla [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2bd72-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd72-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd72-116">Requirements</span></span>



| <span data-ttu-id="2bd72-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd72-117">Requirement</span></span> | <span data-ttu-id="2bd72-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd72-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd72-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd72-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd72-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bd72-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2bd72-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd72-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd72-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2bd72-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2bd72-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd72-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd72-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd72-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd72-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd72-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bd72-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2bd72-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bd72-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2bd72-128">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="2bd72-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




