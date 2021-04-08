---
description: Servizi certificati supporta l'utilizzo di certificati come definito nella raccomandazione ITU-T X. 509 (anche ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Proprietà certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881006"
---
# <a name="certificate-properties"></a><span data-ttu-id="f102a-103">Proprietà certificato</span><span class="sxs-lookup"><span data-stu-id="f102a-103">Certificate Properties</span></span>

<span data-ttu-id="f102a-104">Servizi certificati supporta l'utilizzo di certificati come definito nella raccomandazione ITU-T [*X. 509*](../secgloss/x-gly.md) (anche ISO/IEC 9594-8).</span><span class="sxs-lookup"><span data-stu-id="f102a-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="f102a-105">Di seguito sono riportate le proprietà contenute in un certificato X. 509 standard.</span><span class="sxs-lookup"><span data-stu-id="f102a-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="f102a-106">Campo</span><span class="sxs-lookup"><span data-stu-id="f102a-106">Field</span></span>                                       | <span data-ttu-id="f102a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f102a-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f102a-108">Versione</span><span class="sxs-lookup"><span data-stu-id="f102a-108">Version</span></span>                                     | <span data-ttu-id="f102a-109">Numero di versione del formato del certificato.</span><span class="sxs-lookup"><span data-stu-id="f102a-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f102a-110">Numero di serie</span><span class="sxs-lookup"><span data-stu-id="f102a-110">Serial Number</span></span>                               | <span data-ttu-id="f102a-111">Numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="f102a-111">Serial number of the certificate.</span></span> <span data-ttu-id="f102a-112">Questo numero viene assegnato dall'emittente ed è univoco all'interno dell'elenco dei certificati emessi dall'emittente.</span><span class="sxs-lookup"><span data-stu-id="f102a-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="f102a-113">Identificatore e parametri dell'algoritmo</span><span class="sxs-lookup"><span data-stu-id="f102a-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="f102a-114">Algoritmo di firma e qualsiasi parametro usato dall'emittente.</span><span class="sxs-lookup"><span data-stu-id="f102a-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="f102a-115">Issuer</span><span class="sxs-lookup"><span data-stu-id="f102a-115">Issuer</span></span>                                      | <span data-ttu-id="f102a-116">Nome dell' [*autorità di certificazione*](../secgloss/c-gly.md) che ha emesso il certificato.</span><span class="sxs-lookup"><span data-stu-id="f102a-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="f102a-117">Non prima (Data)</span><span class="sxs-lookup"><span data-stu-id="f102a-117">Not Before (Date)</span></span>                           | <span data-ttu-id="f102a-118">Il certificato non è valido prima di questa data.</span><span class="sxs-lookup"><span data-stu-id="f102a-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="f102a-119">Non dopo (Data)</span><span class="sxs-lookup"><span data-stu-id="f102a-119">Not After (Date)</span></span>                            | <span data-ttu-id="f102a-120">Il certificato non è valido dopo questa data.</span><span class="sxs-lookup"><span data-stu-id="f102a-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="f102a-121">Nome soggetto</span><span class="sxs-lookup"><span data-stu-id="f102a-121">Subject Name</span></span>                                | <span data-ttu-id="f102a-122">Nome della persona o dell'entità a cui viene emesso il certificato.</span><span class="sxs-lookup"><span data-stu-id="f102a-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="f102a-123">Questo campo può includere anche organizzazione del destinatario del certificato, unità organizzativa, località, stato o provincia e paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="f102a-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="f102a-124">Algoritmo e parametri della chiave pubblica dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="f102a-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="f102a-125">Algoritmo e tutti i parametri utilizzati per la [*chiave pubblica*](../secgloss/p-gly.md)del soggetto.</span><span class="sxs-lookup"><span data-stu-id="f102a-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="f102a-126">Chiave pubblica del soggetto</span><span class="sxs-lookup"><span data-stu-id="f102a-126">Subject Public Key</span></span>                          | <span data-ttu-id="f102a-127">Chiave pubblica effettiva, ovvero una stringa di bit.</span><span class="sxs-lookup"><span data-stu-id="f102a-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="f102a-128">Firma</span><span class="sxs-lookup"><span data-stu-id="f102a-128">Signature</span></span>                                   | <span data-ttu-id="f102a-129">Firma fornita dall'emittente.</span><span class="sxs-lookup"><span data-stu-id="f102a-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="f102a-130">Un certificato può contenere gli elementi seguenti, a seconda della versione [*X. 509*](../secgloss/x-gly.md) del certificato.</span><span class="sxs-lookup"><span data-stu-id="f102a-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="f102a-131">Campo facoltativo</span><span class="sxs-lookup"><span data-stu-id="f102a-131">Optional field</span></span>    | <span data-ttu-id="f102a-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f102a-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f102a-133">ID univoco dell'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="f102a-133">Issuer Unique ID</span></span>  | <span data-ttu-id="f102a-134">Utilizzato per rendere non ambiguo il nome dell'autorità emittente se è stato utilizzato da più di un'entità.</span><span class="sxs-lookup"><span data-stu-id="f102a-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="f102a-135">Presente solo nelle versioni [*X. 509*](../secgloss/x-gly.md) 2,0 o successive.</span><span class="sxs-lookup"><span data-stu-id="f102a-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="f102a-136">ID oggetto univoco</span><span class="sxs-lookup"><span data-stu-id="f102a-136">Subject unique ID</span></span> | <span data-ttu-id="f102a-137">Utilizzato per rendere ambiguo il nome del soggetto se è stato utilizzato da più di un'entità.</span><span class="sxs-lookup"><span data-stu-id="f102a-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="f102a-138">Presente solo in X. 509 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f102a-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="f102a-139">Estensioni</span><span class="sxs-lookup"><span data-stu-id="f102a-139">Extensions</span></span>        | <span data-ttu-id="f102a-140">Per specificare le proprietà personalizzate desiderate.</span><span class="sxs-lookup"><span data-stu-id="f102a-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="f102a-141">Il certificato può includere un numero qualsiasi di campi di estensione.</span><span class="sxs-lookup"><span data-stu-id="f102a-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="f102a-142">Presente solo nella versione X. 509 3,0.</span><span class="sxs-lookup"><span data-stu-id="f102a-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="f102a-143">Servizi certificati Microsoft rilascia certificati X. 509 versione 3.</span><span class="sxs-lookup"><span data-stu-id="f102a-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f102a-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f102a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f102a-145">Proprietà nome</span><span class="sxs-lookup"><span data-stu-id="f102a-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
