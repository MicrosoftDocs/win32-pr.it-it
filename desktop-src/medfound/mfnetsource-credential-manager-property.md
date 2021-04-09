---
description: Contiene un puntatore all'interfaccia IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Proprietà MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130115"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="9c02f-103">\_Proprietà di \_ Gestione credenziali MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="9c02f-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="9c02f-104">Contiene un puntatore all'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="9c02f-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="9c02f-105">Usare questa proprietà per passare l'implementazione dell'applicazione di [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) all'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="9c02f-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="9c02f-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9c02f-106">Data type</span></span>

<span data-ttu-id="9c02f-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9c02f-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9c02f-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9c02f-108">PROPVARIANT member</span></span>

<span data-ttu-id="9c02f-109">Puntatore **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="9c02f-109">**IUnknown** pointer</span></span>

<span data-ttu-id="9c02f-110">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="9c02f-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="9c02f-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="9c02f-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9c02f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c02f-112">Remarks</span></span>

<span data-ttu-id="9c02f-113">La costante **MFNETSOURCE \_ Credential \_ Manager** definisce il **GUID** per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="9c02f-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="9c02f-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="9c02f-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c02f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c02f-115">Requirements</span></span>



| <span data-ttu-id="9c02f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c02f-116">Requirement</span></span> | <span data-ttu-id="9c02f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9c02f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c02f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c02f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c02f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c02f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c02f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c02f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c02f-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c02f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c02f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c02f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c02f-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c02f-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c02f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c02f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c02f-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c02f-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9c02f-126">Autenticazione origine rete</span><span class="sxs-lookup"><span data-stu-id="9c02f-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="9c02f-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c02f-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




