---
description: Il valore del campo &\# 0034; c-hostexe&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Proprietà MFNETSOURCE_HOSTEXE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759074"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="a74a7-103">\_Proprietà HOSTEXE di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="a74a7-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="a74a7-104">Valore del campo "c-hostexe" utilizzato dall'origine di rete per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a74a7-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="a74a7-105">Le applicazioni possono impostare questa proprietà sul nome dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="a74a7-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="a74a7-106">Ad esempio, il valore potrebbe essere "iexplore.exe" se l'applicazione è ospitata in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="a74a7-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="a74a7-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a74a7-107">Data type</span></span>

<span data-ttu-id="a74a7-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a74a7-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a74a7-109">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a74a7-109">PROPVARIANT member</span></span>

<span data-ttu-id="a74a7-110">Stringa di caratteri wide (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="a74a7-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="a74a7-111">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="a74a7-111">VT\_LPWSTR</span></span>

<span data-ttu-id="a74a7-112">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="a74a7-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a74a7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a74a7-113">Remarks</span></span>

<span data-ttu-id="a74a7-114">La costante **MFNETSOURCE \_ HOSTEXE** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a74a7-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="a74a7-115">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="a74a7-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a74a7-116">Le applicazioni possono usare questa proprietà per configurare l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="a74a7-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a74a7-117">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="a74a7-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a74a7-118">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a74a7-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a74a7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a74a7-119">Requirements</span></span>



| <span data-ttu-id="a74a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a74a7-120">Requirement</span></span> | <span data-ttu-id="a74a7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a74a7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a74a7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a74a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a74a7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a74a7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a74a7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a74a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a74a7-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a74a7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a74a7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a74a7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74a7-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a74a7-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74a7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a74a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74a7-129">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="a74a7-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="a74a7-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a74a7-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a74a7-131">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a74a7-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




