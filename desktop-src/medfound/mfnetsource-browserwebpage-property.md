---
description: Il valore del campo &\# 0034; CS (Referer) &\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: Proprietà MFNETSOURCE_BROWSERWEBPAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966892"
---
# <a name="mfnetsource_browserwebpage-property"></a><span data-ttu-id="e0f80-103">\_Proprietà BROWSERWEBPAGE di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="e0f80-103">MFNETSOURCE\_BROWSERWEBPAGE property</span></span>

<span data-ttu-id="e0f80-104">Valore del campo "CS (Referer)" utilizzato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e0f80-104">The value of the "cs(Referer)" field that the network source uses for logging.</span></span> <span data-ttu-id="e0f80-105">Le applicazioni possono impostare questa proprietà sull'URL della pagina Web in cui l'applicazione è stata incorporata.</span><span class="sxs-lookup"><span data-stu-id="e0f80-105">Applications can set this property to the URL of the webpage in which the application was embedded.</span></span>



<span data-ttu-id="e0f80-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e0f80-106">Data type</span></span>

<span data-ttu-id="e0f80-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e0f80-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e0f80-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e0f80-108">PROPVARIANT member</span></span>

<span data-ttu-id="e0f80-109">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="e0f80-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="e0f80-110">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="e0f80-110">VT\_LPWSTR</span></span>

<span data-ttu-id="e0f80-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="e0f80-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e0f80-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0f80-112">Remarks</span></span>

<span data-ttu-id="e0f80-113">La costante **MFNETSOURCE \_ BROWSERWEBPAGE** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0f80-113">The constant **MFNETSOURCE\_BROWSERWEBPAGE** defines the GUID for this property key.</span></span> <span data-ttu-id="e0f80-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="e0f80-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e0f80-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="e0f80-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e0f80-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="e0f80-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e0f80-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e0f80-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f80-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0f80-118">Requirements</span></span>



| <span data-ttu-id="e0f80-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f80-119">Requirement</span></span> | <span data-ttu-id="e0f80-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e0f80-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f80-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0f80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f80-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0f80-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0f80-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0f80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f80-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0f80-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0f80-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0f80-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0f80-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0f80-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f80-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0f80-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f80-128">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="e0f80-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="e0f80-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0f80-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e0f80-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0f80-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




