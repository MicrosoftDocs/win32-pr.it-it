---
title: Interfaccia IWMDRMSecurity
description: L'interfaccia IWMDRMSecurity gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema di Digital Rights Management (DRM). Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Formato Windows Media Interface IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334300"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="b7dfc-105">Interfaccia IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="b7dfc-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="b7dfc-106">L'interfaccia **IWMDRMSecurity** gestisce un'ampia gamma di informazioni relative alla sicurezza per il computer client e il sottosistema di Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="b7dfc-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="b7dfc-107">Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="b7dfc-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="b7dfc-108">Passare **IID \_ IWMDRMSecurity** come parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="b7dfc-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="b7dfc-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b7dfc-109">Members</span></span>

<span data-ttu-id="b7dfc-110">L'interfaccia **IWMDRMSecurity** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="b7dfc-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="b7dfc-111">**IWMDRMSecurity** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7dfc-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="b7dfc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7dfc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b7dfc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7dfc-113">Methods</span></span>

<span data-ttu-id="b7dfc-114">L'interfaccia **IWMDRMSecurity** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="b7dfc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b7dfc-115">Method</span></span>                                                                                      | <span data-ttu-id="b7dfc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7dfc-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7dfc-117">**CheckCertForRevocation**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="b7dfc-118">Determina se un certificato è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="b7dfc-119">**GetContentEnablersForRevocations**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="b7dfc-120">Recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="b7dfc-121">**GetContentEnablersFromHashes**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="b7dfc-122">Recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="b7dfc-123">**GetMachineCertificate**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="b7dfc-124">Recupera il certificato del computer del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="b7dfc-125">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="b7dfc-126">Recupera un elenco di revoche di certificati dall'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="b7dfc-127">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="b7dfc-128">Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="b7dfc-129">**GetSecurityVersion**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="b7dfc-130">Recupera la versione del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="b7dfc-131">**PerformSecurityUpdate**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="b7dfc-132">Avvia un aggiornamento della sicurezza del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="b7dfc-133">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="b7dfc-134">Imposta un elenco di revoche di certificati nell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="b7dfc-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="b7dfc-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7dfc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dfc-136">**Esempio di individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="b7dfc-137">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b7dfc-138">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="b7dfc-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





