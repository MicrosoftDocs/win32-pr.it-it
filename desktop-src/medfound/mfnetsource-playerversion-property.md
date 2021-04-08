---
description: Il valore del campo &\# 0034; c-playerversion&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Proprietà MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759668"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="0910d-103">\_Proprietà PLAYERVERSION di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="0910d-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="0910d-104">Valore del campo "c-playerversion" utilizzato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="0910d-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="0910d-105">Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0910d-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="0910d-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0910d-106">Data type</span></span>

<span data-ttu-id="0910d-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0910d-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0910d-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0910d-108">PROPVARIANT member</span></span>

<span data-ttu-id="0910d-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="0910d-109">**LONGLONG**</span></span>

<span data-ttu-id="0910d-110">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="0910d-110">VT\_I8</span></span>

<span data-ttu-id="0910d-111">**hVal**</span><span class="sxs-lookup"><span data-stu-id="0910d-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0910d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0910d-112">Remarks</span></span>

<span data-ttu-id="0910d-113">La costante **MFNETSOURCE \_ PLAYERVERSION** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0910d-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="0910d-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="0910d-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="0910d-115">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="0910d-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="0910d-116">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="0910d-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="0910d-117">Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="0910d-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0910d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0910d-118">Requirements</span></span>



| <span data-ttu-id="0910d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0910d-119">Requirement</span></span> | <span data-ttu-id="0910d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0910d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0910d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0910d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0910d-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0910d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0910d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0910d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0910d-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0910d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0910d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0910d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0910d-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0910d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0910d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0910d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0910d-128">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="0910d-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="0910d-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0910d-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0910d-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0910d-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




