---
description: Il valore del campo &\# 0034; c-hostexever&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Proprietà MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485204"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="32790-103">\_Proprietà HOSTVERSION di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="32790-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="32790-104">Valore del campo "c-hostexever" utilizzato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="32790-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="32790-105">Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="32790-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="32790-106">L'applicazione host è il file con estensione exe identificato dal campo c-hostexe.</span><span class="sxs-lookup"><span data-stu-id="32790-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="32790-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="32790-107">Data type</span></span>

<span data-ttu-id="32790-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="32790-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="32790-109">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="32790-109">PROPVARIANT member</span></span>

<span data-ttu-id="32790-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="32790-110">**LONGLONG**</span></span>

<span data-ttu-id="32790-111">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="32790-111">VT\_I8</span></span>

<span data-ttu-id="32790-112">**hVal**</span><span class="sxs-lookup"><span data-stu-id="32790-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="32790-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="32790-113">Remarks</span></span>

<span data-ttu-id="32790-114">La costante **MFNETSOURCE \_ HOSTVERSION** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="32790-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="32790-115">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="32790-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="32790-116">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="32790-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="32790-117">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="32790-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="32790-118">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="32790-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32790-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32790-119">Requirements</span></span>



| <span data-ttu-id="32790-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32790-120">Requirement</span></span> | <span data-ttu-id="32790-121">Valore</span><span class="sxs-lookup"><span data-stu-id="32790-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32790-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32790-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32790-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32790-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="32790-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32790-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32790-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32790-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="32790-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32790-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32790-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32790-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32790-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32790-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32790-129">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="32790-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="32790-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32790-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="32790-131">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32790-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




