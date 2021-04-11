---
description: La dimensione di una richiesta di accesso digest deve essere inferiore a 2048 byte.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenuto di una richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128315"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="a90c1-103">Contenuto di una richiesta digest</span><span class="sxs-lookup"><span data-stu-id="a90c1-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="a90c1-104">La dimensione di una richiesta di accesso digest deve essere inferiore a 2048 byte.</span><span class="sxs-lookup"><span data-stu-id="a90c1-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="a90c1-105">Nell'esempio seguente viene illustrata una richiesta di verifica assegnata alla stringa di caratteri szChallenge.</span><span class="sxs-lookup"><span data-stu-id="a90c1-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="a90c1-106">La stringa di verifica è racchiusa tra virgolette doppie e contiene virgolette doppie incorporate.</span><span class="sxs-lookup"><span data-stu-id="a90c1-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="a90c1-107">Le virgolette doppie incorporate devono essere precedute (con caratteri di escape) con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="a90c1-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="a90c1-108">Una richiesta digest può contenere le direttive seguenti.</span><span class="sxs-lookup"><span data-stu-id="a90c1-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="a90c1-109">Direttiva</span><span class="sxs-lookup"><span data-stu-id="a90c1-109">Directive</span></span>         | <span data-ttu-id="a90c1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a90c1-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a90c1-111">realm</span><span class="sxs-lookup"><span data-stu-id="a90c1-111">realm</span></span>             | <span data-ttu-id="a90c1-112">Hint definito dall'implementazione per il client su cui sono richieste le [*credenziali*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="a90c1-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="a90c1-113">Se vengono richieste le credenziali, il client deve visualizzare queste informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="a90c1-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="a90c1-114">algoritmo</span><span class="sxs-lookup"><span data-stu-id="a90c1-114">algorithm</span></span>         | <span data-ttu-id="a90c1-115">Microsoft Digest supporta MD5 e MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="a90c1-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="a90c1-116">Per ottenere prestazioni ottimali, usare MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="a90c1-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="a90c1-117">qop</span><span class="sxs-lookup"><span data-stu-id="a90c1-117">qop</span></span>               | <span data-ttu-id="a90c1-118">Questa direttiva può essere impostata su auth, auth-int o auth-conf.</span><span class="sxs-lookup"><span data-stu-id="a90c1-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="a90c1-119">Per ulteriori informazioni, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="a90c1-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="a90c1-120">nonce</span><span class="sxs-lookup"><span data-stu-id="a90c1-120">nonce</span></span>             | <span data-ttu-id="a90c1-121">Valore codificato univoco generato dal server per ogni richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="a90c1-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="a90c1-122">Il valore non deve essere modificato dal client.</span><span class="sxs-lookup"><span data-stu-id="a90c1-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="a90c1-123">opaco</span><span class="sxs-lookup"><span data-stu-id="a90c1-123">opaque</span></span>            | <span data-ttu-id="a90c1-124">Contiene un riferimento per il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) che si sta stabilendo.</span><span class="sxs-lookup"><span data-stu-id="a90c1-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="a90c1-125">Per ulteriori informazioni, vedere [gestione del contesto di sicurezza tra le connessioni](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="a90c1-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="a90c1-126">Cipher (solo SASL)</span><span class="sxs-lookup"><span data-stu-id="a90c1-126">cipher(SASL only)</span></span> | <span data-ttu-id="a90c1-127">Elenco di crittografie supportate dal server.</span><span class="sxs-lookup"><span data-stu-id="a90c1-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="a90c1-128">Questo elemento può essere presente in una richiesta di autenticazione SASL digest solo se la direttiva qop specifica auth-conf.</span><span class="sxs-lookup"><span data-stu-id="a90c1-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="a90c1-129">Per ulteriori informazioni, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="a90c1-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="a90c1-130">charset</span><span class="sxs-lookup"><span data-stu-id="a90c1-130">charset</span></span>           | <span data-ttu-id="a90c1-131">Questa direttiva può essere impostata su UTF-8 se il server è in grado di elaborare i nomi utente e le aree di autenticazione con codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a90c1-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="a90c1-132">Se il client riconosce la direttiva charset, può rispondere usando valori con codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a90c1-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="a90c1-133">Microsoft Digest genera la stringa di verifica del digest per le applicazioni server.</span><span class="sxs-lookup"><span data-stu-id="a90c1-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="a90c1-134">Per informazioni dettagliate, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="a90c1-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
