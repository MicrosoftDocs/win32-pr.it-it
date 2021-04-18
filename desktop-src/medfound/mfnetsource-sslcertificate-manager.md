---
description: Archivia il puntatore IUnknown della classe che implementa l'interfaccia IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Proprietà MFNETSOURCE_SSLCERTIFICATE_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305366"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="f5bf0-103">Proprietà di MFNETSOURCE \_ SSLCERTIFICATE \_ Manager</span><span class="sxs-lookup"><span data-stu-id="f5bf0-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="f5bf0-104">Archivia il puntatore **IUnknown** della classe che implementa l'interfaccia [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) .</span><span class="sxs-lookup"><span data-stu-id="f5bf0-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="f5bf0-105">L'implementazione client fornisce metodi per ottenere il certificato SSL del client quando viene richiesto dal server.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="f5bf0-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5bf0-106">Data type</span></span>

<span data-ttu-id="f5bf0-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f5bf0-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f5bf0-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f5bf0-108">PROPVARIANT member</span></span>

<span data-ttu-id="f5bf0-109">**Puntatore IUnknown**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-109">**IUnknown pointer**</span></span>

<span data-ttu-id="f5bf0-110">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f5bf0-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="f5bf0-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f5bf0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5bf0-112">Remarks</span></span>

<span data-ttu-id="f5bf0-113">La costante **MFNETSOURCE \_ SSLCERTIFICATE \_ Manager** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="f5bf0-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="f5bf0-115">Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f5bf0-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f5bf0-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bf0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5bf0-117">Requirements</span></span>



| <span data-ttu-id="f5bf0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5bf0-118">Requirement</span></span> | <span data-ttu-id="f5bf0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f5bf0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bf0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5bf0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bf0-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f5bf0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5bf0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bf0-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f5bf0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5bf0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5bf0-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bf0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5bf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bf0-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5bf0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f5bf0-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5bf0-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




