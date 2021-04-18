---
description: Specifica se il protocollo multicast MSB (Media Stream Broadcast) è abilitato nell'origine di rete.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: Proprietà MFNETSOURCE_ENABLE_MSB (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308403"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="7f929-103">MFNETSOURCE \_ Abilita \_ Proprietà MSB</span><span class="sxs-lookup"><span data-stu-id="7f929-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="7f929-104">Specifica se il protocollo multicast MSB (Media Stream Broadcast) è abilitato nell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="7f929-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="7f929-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f929-105">Data type</span></span>

<span data-ttu-id="7f929-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="7f929-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7f929-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="7f929-107">PROPVARIANT member</span></span>

<span data-ttu-id="7f929-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="7f929-108">**LONG**</span></span>

<span data-ttu-id="7f929-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7f929-109">VT\_I4</span></span>

<span data-ttu-id="7f929-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="7f929-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="7f929-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f929-111">Remarks</span></span>

<span data-ttu-id="7f929-112">La costante **MFNETSOURCE \_ enable \_ MSB** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f929-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="7f929-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="7f929-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="7f929-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="7f929-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="7f929-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="7f929-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="7f929-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="7f929-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f929-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f929-117">Requirements</span></span>



| <span data-ttu-id="7f929-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f929-118">Requirement</span></span> | <span data-ttu-id="7f929-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7f929-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f929-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f929-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f929-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f929-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f929-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f929-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f929-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f929-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7f929-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f929-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f929-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f929-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f929-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f929-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f929-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f929-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7f929-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f929-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7f929-129">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="7f929-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




