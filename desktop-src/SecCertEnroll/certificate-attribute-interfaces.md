---
description: Per creare attributi di certificato, è possibile usare le interfacce seguenti.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfacce degli attributi di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307226"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="d9195-103">Interfacce degli attributi di certificato</span><span class="sxs-lookup"><span data-stu-id="d9195-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="d9195-104">Per creare attributi di certificato, è possibile usare le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9195-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="d9195-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="d9195-105">Interface</span></span>                                                                    | <span data-ttu-id="d9195-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9195-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9195-107">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="d9195-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="d9195-108">Rappresenta un attributo di crittografia in una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="d9195-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="d9195-109">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="d9195-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="d9195-110">Gestisce una raccolta di oggetti [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="d9195-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="d9195-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="d9195-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="d9195-112">Rappresenta un attributo in una \# richiesta di certificato PKCS 7, PKCS \# 10 o CMC.</span><span class="sxs-lookup"><span data-stu-id="d9195-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="d9195-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="d9195-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="d9195-114">Rappresenta un attributo che può essere utilizzato per identificare il client che ha generato una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="d9195-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="d9195-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="d9195-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="d9195-116">Rappresenta le estensioni del certificato in una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="d9195-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="d9195-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="d9195-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="d9195-118">Rappresenta un attributo che contiene una chiave privata crittografata che deve essere archiviata da un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="d9195-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="d9195-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="d9195-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="d9195-120">Rappresenta un attributo che contiene un hash SHA-1 della chiave privata crittografata da archiviare da un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="d9195-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="d9195-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="d9195-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="d9195-122">Rappresenta un attributo che identifica il provider di crittografia utilizzato dall'entità che richiede il certificato.</span><span class="sxs-lookup"><span data-stu-id="d9195-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="d9195-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="d9195-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="d9195-124">Rappresenta un attributo che contiene le informazioni sulla versione relative al sistema operativo client in cui è stata generata la richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="d9195-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="d9195-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="d9195-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="d9195-126">Rappresenta un attributo che contiene il certificato da rinnovare.</span><span class="sxs-lookup"><span data-stu-id="d9195-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="d9195-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="d9195-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="d9195-128">Gestisce una raccolta di oggetti [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="d9195-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="d9195-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="d9195-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="d9195-130">Rappresenta una coppia nome-valore generica.</span><span class="sxs-lookup"><span data-stu-id="d9195-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="d9195-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="d9195-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="d9195-132">Gestisce una raccolta di oggetti [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="d9195-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d9195-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9195-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9195-134">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="d9195-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



