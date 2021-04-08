---
description: Il valore del campo &\# 0034; c-playerid&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: Proprietà MFNETSOURCE_PLAYERID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057912"
---
# <a name="mfnetsource_playerid-property"></a><span data-ttu-id="59267-103">\_Proprietà playerid di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="59267-103">MFNETSOURCE\_PLAYERID property</span></span>

<span data-ttu-id="59267-104">Valore del campo "c-playerid" utilizzato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="59267-104">The value of the "c-playerid" field that the network source uses for logging.</span></span> <span data-ttu-id="59267-105">Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.</span><span class="sxs-lookup"><span data-stu-id="59267-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="59267-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="59267-106">Data type</span></span>

<span data-ttu-id="59267-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="59267-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="59267-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="59267-108">PROPVARIANT member</span></span>

<span data-ttu-id="59267-109">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="59267-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="59267-110">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="59267-110">VT\_LPWSTR</span></span>

<span data-ttu-id="59267-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="59267-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="59267-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="59267-112">Remarks</span></span>

<span data-ttu-id="59267-113">La costante **MFNETSOURCE \_ playerid** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="59267-113">The constant **MFNETSOURCE\_PLAYERID** defines the GUID for this property key.</span></span> <span data-ttu-id="59267-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="59267-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="59267-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="59267-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="59267-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="59267-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="59267-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="59267-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59267-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59267-118">Requirements</span></span>



| <span data-ttu-id="59267-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="59267-119">Requirement</span></span> | <span data-ttu-id="59267-120">Valore</span><span class="sxs-lookup"><span data-stu-id="59267-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59267-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59267-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59267-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59267-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59267-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59267-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59267-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59267-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59267-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59267-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="59267-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59267-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59267-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59267-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59267-128">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="59267-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="59267-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59267-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="59267-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59267-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




