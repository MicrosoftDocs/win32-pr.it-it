---
description: Il valore della prima parte del \# campo &0034; CS (User-Agent) &\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Proprietà MFNETSOURCE_BROWSERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527385"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="eedb4-103">\_Proprietà BROWSERUSERAGENT di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="eedb4-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="eedb4-104">Il valore della prima parte del campo "CS (User-Agent)" usato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="eedb4-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="eedb4-105">Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.</span><span class="sxs-lookup"><span data-stu-id="eedb4-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="eedb4-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eedb4-106">Data type</span></span>

<span data-ttu-id="eedb4-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="eedb4-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="eedb4-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="eedb4-108">PROPVARIANT member</span></span>

<span data-ttu-id="eedb4-109">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="eedb4-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="eedb4-110">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="eedb4-110">VT\_LPWSTR</span></span>

<span data-ttu-id="eedb4-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="eedb4-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="eedb4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="eedb4-112">Remarks</span></span>

<span data-ttu-id="eedb4-113">La costante **MFNETSOURCE \_ BROWSERUSERAGENT** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="eedb4-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="eedb4-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="eedb4-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="eedb4-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="eedb4-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="eedb4-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="eedb4-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="eedb4-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="eedb4-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eedb4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eedb4-118">Requirements</span></span>



| <span data-ttu-id="eedb4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eedb4-119">Requirement</span></span> | <span data-ttu-id="eedb4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="eedb4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eedb4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eedb4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eedb4-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eedb4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eedb4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eedb4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eedb4-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eedb4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eedb4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eedb4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eedb4-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eedb4-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedb4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eedb4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedb4-128">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="eedb4-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="eedb4-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eedb4-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="eedb4-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eedb4-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eedb4-131">**\_PLAYERUSERAGENT MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="eedb4-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




