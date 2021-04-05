---
description: Gli attributi possono essere aggiunti a una richiesta di certificato per fornire un'autorità di certificazione (CA) con informazioni aggiuntive che possono essere utilizzate durante la creazione e l'emissione di un certificato.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753482"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="67a9e-103">Attributi (API di registrazione certificati)</span><span class="sxs-lookup"><span data-stu-id="67a9e-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="67a9e-104">Gli attributi possono essere aggiunti a una richiesta di certificato per fornire un'autorità di certificazione (CA) con informazioni aggiuntive che possono essere utilizzate durante la creazione e l'emissione di un certificato.</span><span class="sxs-lookup"><span data-stu-id="67a9e-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="67a9e-105">Ogni attributo è una struttura ad [*albero*](/windows/desktop/SecGloss/a-gly) (ASN. 1) codificata [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) che contiene un identificatore di oggetto (OID) e zero o più valori.</span><span class="sxs-lookup"><span data-stu-id="67a9e-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="67a9e-106">Gli attributi vengono definiti usando le interfacce incluse con l'API di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="67a9e-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="67a9e-107">Gli argomenti seguenti illustrano gli attributi in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="67a9e-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="67a9e-108">Attributi supportati</span><span class="sxs-lookup"><span data-stu-id="67a9e-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="67a9e-109">Architettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="67a9e-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="67a9e-110">\#Attributi PKCS 7</span><span class="sxs-lookup"><span data-stu-id="67a9e-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="67a9e-111">\#Attributi PKCS 10</span><span class="sxs-lookup"><span data-stu-id="67a9e-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="67a9e-112">Attributi CMC</span><span class="sxs-lookup"><span data-stu-id="67a9e-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
