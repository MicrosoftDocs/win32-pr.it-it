---
description: Matrice di stringhe con i parametri da inviare al server di log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Proprietà MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967036"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="cb45d-103">\_Proprietà LOGPARAMS di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="cb45d-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="cb45d-104">Matrice di stringhe con i parametri da inviare al server di log.</span><span class="sxs-lookup"><span data-stu-id="cb45d-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="cb45d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cb45d-105">Data type</span></span>

<span data-ttu-id="cb45d-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="cb45d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="cb45d-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="cb45d-107">PROPVARIANT member</span></span>

<span data-ttu-id="cb45d-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="cb45d-108">\**WCHAR\** _</span></span>

<span data-ttu-id="cb45d-109">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="cb45d-109">VT\_LPWSTR</span></span>

<span data-ttu-id="cb45d-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="cb45d-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="cb45d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb45d-111">Remarks</span></span>

<span data-ttu-id="cb45d-112">La costante **MFNETSOURCE \_ LOGPARAMS** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cb45d-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="cb45d-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="cb45d-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="cb45d-114">Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="cb45d-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="cb45d-115">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="cb45d-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb45d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb45d-116">Requirements</span></span>



| <span data-ttu-id="cb45d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb45d-117">Requirement</span></span> | <span data-ttu-id="cb45d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cb45d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb45d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb45d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb45d-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb45d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cb45d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb45d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb45d-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb45d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cb45d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb45d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb45d-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb45d-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb45d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb45d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb45d-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb45d-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cb45d-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb45d-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




