---
description: Specifica se il contenuto viene memorizzato nella cache dell'origine di rete.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Proprietà MFNETSOURCE_CACHEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879806"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="a8ea8-103">\_Proprietà CACHEENABLED di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="a8ea8-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="a8ea8-104">Specifica se il contenuto viene memorizzato nella cache dell'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="a8ea8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a8ea8-105">Data type</span></span>

<span data-ttu-id="a8ea8-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a8ea8-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a8ea8-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a8ea8-107">PROPVARIANT member</span></span>

<span data-ttu-id="a8ea8-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="a8ea8-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="a8ea8-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a8ea8-109">VT\_I4</span></span>

<span data-ttu-id="a8ea8-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="a8ea8-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a8ea8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8ea8-111">Remarks</span></span>

<span data-ttu-id="a8ea8-112">La costante **MFNETSOURCE \_ CACHEENABLED** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="a8ea8-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a8ea8-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a8ea8-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a8ea8-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a8ea8-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="a8ea8-117">Il valore predefinito di questa proprietà è **true**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ea8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8ea8-118">Requirements</span></span>



| <span data-ttu-id="a8ea8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ea8-119">Requirement</span></span> | <span data-ttu-id="a8ea8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a8ea8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ea8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8ea8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ea8-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8ea8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8ea8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8ea8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ea8-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8ea8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a8ea8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8ea8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8ea8-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ea8-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ea8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8ea8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ea8-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8ea8-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a8ea8-129">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8ea8-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




