---
description: È possibile usare l'interfaccia IX500DistinguishedName per creare un nome soggetto da una stringa del nome distinto.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Creazione di un nome soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525098"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="0d71c-103">Creazione di un nome soggetto</span><span class="sxs-lookup"><span data-stu-id="0d71c-103">Creating a Subject Name</span></span>

<span data-ttu-id="0d71c-104">È possibile usare l'interfaccia [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) per creare un nome soggetto da una stringa del nome distinto.</span><span class="sxs-lookup"><span data-stu-id="0d71c-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="0d71c-105">La stringa è costituita da nomi distinti relativi concatenati (RDNs).</span><span class="sxs-lookup"><span data-stu-id="0d71c-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="0d71c-106">Le chiavi RDN seguenti sono supportate dall'API di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="0d71c-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="0d71c-107">Chiave</span><span class="sxs-lookup"><span data-stu-id="0d71c-107">Key</span></span>                               | <span data-ttu-id="0d71c-108">OID</span><span class="sxs-lookup"><span data-stu-id="0d71c-108">OID</span></span>                                             | <span data-ttu-id="0d71c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d71c-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d71c-110">C</span><span class="sxs-lookup"><span data-stu-id="0d71c-110">C</span></span><br/>                      | <span data-ttu-id="0d71c-111">\_nome del \_ paese \_ OID XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="0d71c-112">Contiene un codice paese o area ISO 3166 di due lettere.</span><span class="sxs-lookup"><span data-stu-id="0d71c-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="0d71c-113">CN</span><span class="sxs-lookup"><span data-stu-id="0d71c-113">CN</span></span><br/>                     | <span data-ttu-id="0d71c-114">\_ \_ nome comune OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="0d71c-115">Contiene un nome comune.</span><span class="sxs-lookup"><span data-stu-id="0d71c-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="0d71c-116">E</span><span class="sxs-lookup"><span data-stu-id="0d71c-116">E</span></span><br/> <span data-ttu-id="0d71c-117">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="0d71c-117">EMAIL</span></span><br/>     | <span data-ttu-id="0d71c-118">\_OID XCN \_ RSA \_ emailAddr</span><span class="sxs-lookup"><span data-stu-id="0d71c-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="0d71c-119">Contiene un indirizzo di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="0d71c-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="0d71c-120">DC</span><span class="sxs-lookup"><span data-stu-id="0d71c-120">DC</span></span><br/>                     | <span data-ttu-id="0d71c-121">\_componente di \_ dominio \_ OID XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="0d71c-122">Contiene una parte di un nome di Domain Name System (DNS).</span><span class="sxs-lookup"><span data-stu-id="0d71c-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="0d71c-123">G</span><span class="sxs-lookup"><span data-stu-id="0d71c-123">G</span></span><br/> <span data-ttu-id="0d71c-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="0d71c-124">GivenName</span></span><br/> | <span data-ttu-id="0d71c-125">\_nome OID \_ XCN \_</span><span class="sxs-lookup"><span data-stu-id="0d71c-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="0d71c-126">Contiene la parte del nome di una persona che non è un cognome.</span><span class="sxs-lookup"><span data-stu-id="0d71c-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="0d71c-127">I</span><span class="sxs-lookup"><span data-stu-id="0d71c-127">I</span></span><br/>                      | <span data-ttu-id="0d71c-128">\_iniziali OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="0d71c-129">Contiene le iniziali di una persona.</span><span class="sxs-lookup"><span data-stu-id="0d71c-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="0d71c-130">L</span><span class="sxs-lookup"><span data-stu-id="0d71c-130">L</span></span><br/>                      | <span data-ttu-id="0d71c-131">nome della località di XCN \_ OID \_ \_</span><span class="sxs-lookup"><span data-stu-id="0d71c-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="0d71c-132">Contiene il nome della località che identifica una città, un paese o un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="0d71c-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="0d71c-133">O</span><span class="sxs-lookup"><span data-stu-id="0d71c-133">O</span></span><br/>                      | <span data-ttu-id="0d71c-134">\_ \_ nome organizzazione OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="0d71c-135">Contiene il nome di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d71c-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="0d71c-136">OU</span><span class="sxs-lookup"><span data-stu-id="0d71c-136">OU</span></span><br/>                     | <span data-ttu-id="0d71c-137">\_ \_ \_ nome unità organizzativa OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="0d71c-138">Contiene il nome di una suddivisione di unità in un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d71c-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="0d71c-139">S</span><span class="sxs-lookup"><span data-stu-id="0d71c-139">S</span></span><br/> <span data-ttu-id="0d71c-140">ST</span><span class="sxs-lookup"><span data-stu-id="0d71c-140">ST</span></span><br/>        | <span data-ttu-id="0d71c-141">\_nome della \_ \_ provincia o \_ dello stato OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="0d71c-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="0d71c-142">Contiene il nome completo di uno stato o di una provincia.</span><span class="sxs-lookup"><span data-stu-id="0d71c-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="0d71c-143">STREET</span><span class="sxs-lookup"><span data-stu-id="0d71c-143">STREET</span></span><br/>                 | <span data-ttu-id="0d71c-144">XCN \_ OID \_ via \_</span><span class="sxs-lookup"><span data-stu-id="0d71c-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="0d71c-145">Contiene l'indirizzo fisico.</span><span class="sxs-lookup"><span data-stu-id="0d71c-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="0d71c-146">SN</span><span class="sxs-lookup"><span data-stu-id="0d71c-146">SN</span></span><br/>                     | <span data-ttu-id="0d71c-147">\_nome XCN OID \_ sur \_</span><span class="sxs-lookup"><span data-stu-id="0d71c-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="0d71c-148">Contiene il nome della famiglia di una persona.</span><span class="sxs-lookup"><span data-stu-id="0d71c-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="0d71c-149">T</span><span class="sxs-lookup"><span data-stu-id="0d71c-149">T</span></span><br/> <span data-ttu-id="0d71c-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="0d71c-150">TITLE</span></span><br/>     | <span data-ttu-id="0d71c-151">\_titolo OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="0d71c-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="0d71c-152">Contiene il titolo di una persona dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d71c-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="0d71c-153">Quando si Inizializza un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , è possibile identificare il formato del nome distinto specificando un valore del tipo di enumerazione [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) .</span><span class="sxs-lookup"><span data-stu-id="0d71c-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="0d71c-154">Si supponga, ad esempio, che il nome distinto del soggetto sia costituito dai seguenti RDNs:</span><span class="sxs-lookup"><span data-stu-id="0d71c-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="0d71c-155">CN = amministratore</span><span class="sxs-lookup"><span data-stu-id="0d71c-155">CN=Administrator</span></span>  
<span data-ttu-id="0d71c-156">CN = utenti</span><span class="sxs-lookup"><span data-stu-id="0d71c-156">CN=Users</span></span>  
<span data-ttu-id="0d71c-157">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="0d71c-157">DC=jdomcsc</span></span>  
<span data-ttu-id="0d71c-158">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="0d71c-158">DC=nttest</span></span>  
<span data-ttu-id="0d71c-159">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="0d71c-159">DC=microsoft</span></span>  
<span data-ttu-id="0d71c-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="0d71c-160">DC=com</span></span>  
</dl>

<span data-ttu-id="0d71c-161">Se si concatenano questi RDNs nella seguente stringa del nome distinto delimitato da virgole, è possibile specificare il valore del **\_ \_ \_ \_ \_ flag virgola Str del nome del certificato XCN** per l'inizializzazione di un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="0d71c-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="0d71c-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d71c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d71c-163">Codifica di un nome soggetto</span><span class="sxs-lookup"><span data-stu-id="0d71c-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="0d71c-164">Nomi soggetto</span><span class="sxs-lookup"><span data-stu-id="0d71c-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




