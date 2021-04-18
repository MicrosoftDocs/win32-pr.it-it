---
description: Specifica se l'origine di rete invia le richieste di reinvio UDP in risposta a pacchetti persi.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: Proprietà MFNETSOURCE_RESENDSENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309532"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="7b01b-103">\_Proprietà RESENDSENABLED di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="7b01b-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="7b01b-104">Specifica se l'origine di rete invia le richieste di reinvio UDP in risposta a pacchetti persi.</span><span class="sxs-lookup"><span data-stu-id="7b01b-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="7b01b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7b01b-105">Data type</span></span>

<span data-ttu-id="7b01b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="7b01b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7b01b-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="7b01b-107">PROPVARIANT member</span></span>

<span data-ttu-id="7b01b-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="7b01b-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="7b01b-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7b01b-109">VT\_I4</span></span>

<span data-ttu-id="7b01b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="7b01b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="7b01b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b01b-111">Remarks</span></span>

<span data-ttu-id="7b01b-112">La costante **MFNETSOURCE \_ RESENDSENABLED** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b01b-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="7b01b-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="7b01b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="7b01b-114">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="7b01b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="7b01b-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="7b01b-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="7b01b-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="7b01b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="7b01b-117">Il valore predefinito di questa proprietà è **true**.</span><span class="sxs-lookup"><span data-stu-id="7b01b-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b01b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b01b-118">Requirements</span></span>



| <span data-ttu-id="7b01b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b01b-119">Requirement</span></span> | <span data-ttu-id="7b01b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7b01b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b01b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b01b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b01b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b01b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7b01b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b01b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b01b-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b01b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7b01b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b01b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b01b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b01b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b01b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b01b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b01b-128">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="7b01b-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="7b01b-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b01b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7b01b-130">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b01b-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




