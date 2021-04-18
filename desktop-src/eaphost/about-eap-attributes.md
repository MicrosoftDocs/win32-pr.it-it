---
title: Attributi EAP
description: È una \_ struttura di attributi EAP che contiene un tipo di dati predeterminato relativo a una sessione di autenticazione.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300722"
---
# <a name="eap-attributes"></a><span data-ttu-id="3f570-103">Attributi EAP</span><span class="sxs-lookup"><span data-stu-id="3f570-103">EAP Attributes</span></span>

<span data-ttu-id="3f570-104">Un attributo EAP è una struttura dell' [**\_ attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) che contiene un tipo di dati predeterminato relativo a una sessione di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3f570-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="3f570-105">Gli attributi vengono usati per comunicare le informazioni tra i metodi EAP e i supplicant o tra i metodi e gli autenticatori EAP.</span><span class="sxs-lookup"><span data-stu-id="3f570-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="3f570-106">Le implementazioni peer e Authenticator di un metodo EAP possono scambiare questi attributi in una rete.</span><span class="sxs-lookup"><span data-stu-id="3f570-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="3f570-107">Nell'argomento [**\_ \_ tipo di attributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)viene visualizzato un elenco completo dei tipi di attributo supportati.</span><span class="sxs-lookup"><span data-stu-id="3f570-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="3f570-108">Attributi utilizzati dai supplicant</span><span class="sxs-lookup"><span data-stu-id="3f570-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="3f570-109">I tipi di attributo seguenti vengono utilizzati dai supplicant 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="3f570-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="3f570-110">**eatVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="3f570-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="3f570-111">I tipi di attributo seguenti vengono utilizzati dai supplicant client PPP.</span><span class="sxs-lookup"><span data-stu-id="3f570-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="3f570-112">**eatMinimum**</span><span class="sxs-lookup"><span data-stu-id="3f570-112">**eatMinimum**</span></span>
-   <span data-ttu-id="3f570-113">**eatEAPTLV**</span><span class="sxs-lookup"><span data-stu-id="3f570-113">**eatEAPTLV**</span></span>

<span data-ttu-id="3f570-114">I tipi di attributo seguenti vengono utilizzati dai supplicant server PPP.</span><span class="sxs-lookup"><span data-stu-id="3f570-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="3f570-115">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3f570-115">**eatUserName**</span></span>
-   <span data-ttu-id="3f570-116">**eatReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="3f570-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="3f570-117">**eatState**</span><span class="sxs-lookup"><span data-stu-id="3f570-117">**eatState**</span></span>
-   <span data-ttu-id="3f570-118">**eatSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="3f570-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="3f570-119">**eatEAPMessage**</span><span class="sxs-lookup"><span data-stu-id="3f570-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="3f570-120">Attributi esportati dai metodi</span><span class="sxs-lookup"><span data-stu-id="3f570-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="3f570-121">I tipi di attributo seguenti possono essere esportati dai metodi EAP.</span><span class="sxs-lookup"><span data-stu-id="3f570-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="3f570-122">**eatClearTextPassword**</span><span class="sxs-lookup"><span data-stu-id="3f570-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="3f570-123">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="3f570-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="3f570-124">**eatMethodId**</span><span class="sxs-lookup"><span data-stu-id="3f570-124">**eatMethodId**</span></span>

<span data-ttu-id="3f570-125">Il tipo di attributo seguente viene esportato dai metodi [TLS (Transport Level Security](/previous-versions/windows/embedded/ms885336(v=msdn.10)) ) EAP (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="3f570-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="3f570-126">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="3f570-126">**eatCertificateOID**</span></span>

<span data-ttu-id="3f570-127">I tipi di attributo seguenti sono esportati dai metodi [Microsoft Challenge Handshake Authentication Protocol versione 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="3f570-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="3f570-128">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3f570-128">**eatUserName**</span></span>
-   <span data-ttu-id="3f570-129">**eatCredentialsChanged**</span><span class="sxs-lookup"><span data-stu-id="3f570-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="3f570-130">Il tipo di attributo seguente viene utilizzato da server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="3f570-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="3f570-131">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="3f570-131">**eatCertificateOID**</span></span>

<span data-ttu-id="3f570-132">I tipi di attributo seguenti sono esportati da metodi [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3f570-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="3f570-133">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="3f570-133">**eatUserName**</span></span>
-   <span data-ttu-id="3f570-134">**eatPEAPEmbeddedEAPTypeId**</span><span class="sxs-lookup"><span data-stu-id="3f570-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="3f570-135">**eatPEAPFastRoamedSession**</span><span class="sxs-lookup"><span data-stu-id="3f570-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="3f570-136">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="3f570-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f570-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f570-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f570-138">**\_attributo EAP**</span><span class="sxs-lookup"><span data-stu-id="3f570-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="3f570-139">**\_tipo di attributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="3f570-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 