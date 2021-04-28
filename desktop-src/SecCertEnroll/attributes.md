---
description: "Attributi (API di registrazione certificati): è possibile aggiungere attributi a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato."
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributi (API di registrazione certificati)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118429"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="d9124-103">Attributi (API di registrazione certificati)</span><span class="sxs-lookup"><span data-stu-id="d9124-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="d9124-104">È possibile aggiungere attributi a una richiesta di certificato per fornire a un'autorità di certificazione (CA) informazioni aggiuntive che può usare durante la creazione e il rilascio di un certificato.</span><span class="sxs-lookup"><span data-stu-id="d9124-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="d9124-105">Ogni attributo è una [*struttura*](/windows/desktop/SecGloss/d-gly) ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) codificata Distinguished Encoding Rules (DER) che contiene un identificatore di oggetto (OID) e zero o più valori.</span><span class="sxs-lookup"><span data-stu-id="d9124-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="d9124-106">Gli attributi vengono definiti usando le interfacce incluse nell'API di registrazione certificati.</span><span class="sxs-lookup"><span data-stu-id="d9124-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="d9124-107">Gli argomenti seguenti illustrano gli attributi in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="d9124-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="d9124-108">Attributi supportati</span><span class="sxs-lookup"><span data-stu-id="d9124-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="d9124-109">Architettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="d9124-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="d9124-110">Attributi PKCS \# 7</span><span class="sxs-lookup"><span data-stu-id="d9124-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="d9124-111">Attributi PKCS \# 10</span><span class="sxs-lookup"><span data-stu-id="d9124-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="d9124-112">Attributi CMC</span><span class="sxs-lookup"><span data-stu-id="d9124-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
