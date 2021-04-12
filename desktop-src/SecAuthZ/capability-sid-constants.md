---
description: Definire per le funzionalità note per le applicazioni tramite la funzione AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Costanti SID della funzionalità (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234333"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="8377d-103">Costanti SID funzionalità</span><span class="sxs-lookup"><span data-stu-id="8377d-103">Capability SID Constants</span></span>

<span data-ttu-id="8377d-104">Le costanti SID della funzionalità definiscono per le funzionalità note di applicazioni tramite la funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="8377d-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="8377d-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_ \_ client Internet funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-106">(0x00000001L)</span><span class="sxs-lookup"><span data-stu-id="8377d-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-107">Un account ha accesso a Internet da un computer client.</span><span class="sxs-lookup"><span data-stu-id="8377d-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_funzionalità di \_ sicurezza \_ server client Internet \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-109">(0x00000002L)</span><span class="sxs-lookup"><span data-stu-id="8377d-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-110">Un account ha accesso a Internet dai computer client e server.</span><span class="sxs-lookup"><span data-stu-id="8377d-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_funzionalità di \_ sicurezza \_ \_ server client di rete privata \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-112">(0x00000003L)</span><span class="sxs-lookup"><span data-stu-id="8377d-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-113">Un account ha accesso a Internet da una rete privata.</span><span class="sxs-lookup"><span data-stu-id="8377d-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_ \_ Libreria immagini per le funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-115">(0x00000004L)</span><span class="sxs-lookup"><span data-stu-id="8377d-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-116">Un account può accedere alla raccolta immagini.</span><span class="sxs-lookup"><span data-stu-id="8377d-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_ \_ libreria video sulle funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-118">(0x00000005L)</span><span class="sxs-lookup"><span data-stu-id="8377d-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-119">Un account può accedere alla raccolta video.</span><span class="sxs-lookup"><span data-stu-id="8377d-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_ \_ libreria musicale della funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-121">(0x00000006L)</span><span class="sxs-lookup"><span data-stu-id="8377d-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-122">Un account può accedere alla raccolta musicale.</span><span class="sxs-lookup"><span data-stu-id="8377d-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_ \_ raccolta documenti funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-124">(0x00000007L)</span><span class="sxs-lookup"><span data-stu-id="8377d-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-125">Un account ha accesso alla libreria della documentazione di.</span><span class="sxs-lookup"><span data-stu-id="8377d-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_ \_ autenticazione Enterprise per le funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-127">(0x00000008L)</span><span class="sxs-lookup"><span data-stu-id="8377d-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-128">Un account ha accesso alle credenziali di Windows predefinite.</span><span class="sxs-lookup"><span data-stu-id="8377d-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_funzionalità di \_ sicurezza \_ certificati utente condivisi \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-130">(0x00000009L)</span><span class="sxs-lookup"><span data-stu-id="8377d-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-131">Un account può accedere ai certificati utente condivisi.</span><span class="sxs-lookup"><span data-stu-id="8377d-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8377d-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ archiviazione rimovibile della funzionalità di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="8377d-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8377d-133">(0x0000000AL)</span><span class="sxs-lookup"><span data-stu-id="8377d-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="8377d-134">Un account può accedere all'archiviazione rimovibile.</span><span class="sxs-lookup"><span data-stu-id="8377d-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8377d-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="8377d-135">Remarks</span></span>

<span data-ttu-id="8377d-136">Quando si costruisce un SID di funzionalità, è necessario includere l'autorità del pacchetto di sicurezza del \_ pacchetto dell'app \_ \_ {0,0,0,0,0,15} nella chiamata alla funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="8377d-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="8377d-137">Inoltre, è necessario il conteggio RID di base e RID per le funzionalità predefinite, SECURITY \_ Capability \_ base \_ RID (0X00000003L) e Security \_ Builtin \_ Capability \_ RID \_ Count (2L).</span><span class="sxs-lookup"><span data-stu-id="8377d-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="8377d-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8377d-138">Requirements</span></span>



| <span data-ttu-id="8377d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8377d-139">Requirement</span></span> | <span data-ttu-id="8377d-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8377d-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8377d-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8377d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8377d-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8377d-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8377d-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8377d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8377d-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8377d-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8377d-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8377d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8377d-146"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="8377d-146"><dt>Winnt.h</dt></span></span> </dl> |



 

