---
description: Il materiale seguente è valido solo quando il digest viene usato come meccanismo SASL. Le crittografie e la crittografia non sono disponibili per l'autenticazione HTTP con Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226853"
---
# <a name="ciphers"></a><span data-ttu-id="78cde-104">Ciphers</span><span class="sxs-lookup"><span data-stu-id="78cde-104">Ciphers</span></span>

<span data-ttu-id="78cde-105">Il materiale seguente è valido solo quando il digest viene usato come meccanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="78cde-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="78cde-106">Le crittografie e la crittografia non sono disponibili per l'autenticazione HTTP con Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="78cde-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="78cde-107">La direttiva di crittografia di una richiesta digest SASL contiene un elenco delle crittografie supportate da un server che richiede comunicazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="78cde-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="78cde-108">La direttiva di crittografia può essere inclusa solo se la direttiva qop è impostata su "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="78cde-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="78cde-109">Le crittografie riconosciute da Microsoft Digest sono elencate nella tabella seguente, in ordine dal più forte al più debole.</span><span class="sxs-lookup"><span data-stu-id="78cde-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="78cde-110">Valore di crittografia</span><span class="sxs-lookup"><span data-stu-id="78cde-110">Cipher value</span></span> | <span data-ttu-id="78cde-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78cde-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78cde-112">RC4</span><span class="sxs-lookup"><span data-stu-id="78cde-112">"rc4"</span></span>        | <span data-ttu-id="78cde-113">Crittografia RC4 con una chiave a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="78cde-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="78cde-114">3DES</span><span class="sxs-lookup"><span data-stu-id="78cde-114">"3des"</span></span>       | <span data-ttu-id="78cde-115">La crittografia [*triple des*](/windows/desktop/SecGloss/t-gly) in modalità [*CBC*](/windows/desktop/SecGloss/c-gly) con Ede con la stessa chiave per ogni fase E (modalità a due chiavi).</span><span class="sxs-lookup"><span data-stu-id="78cde-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="78cde-116">La lunghezza totale della chiave è 112 bit.</span><span class="sxs-lookup"><span data-stu-id="78cde-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="78cde-117">"RC4-56"</span><span class="sxs-lookup"><span data-stu-id="78cde-117">"rc4-56"</span></span>     | <span data-ttu-id="78cde-118">Crittografia RC4 con una chiave a 56 bit.</span><span class="sxs-lookup"><span data-stu-id="78cde-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="78cde-119">"RC4-40"</span><span class="sxs-lookup"><span data-stu-id="78cde-119">"rc4-40"</span></span>     | <span data-ttu-id="78cde-120">Crittografia RC4 con una chiave a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="78cde-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="78cde-121">des</span><span class="sxs-lookup"><span data-stu-id="78cde-121">"des"</span></span>        | <span data-ttu-id="78cde-122">Crittografia DES ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) in modalità CBC ( [*Cipher Block Chaining*](/windows/desktop/SecGloss/c-gly) ) con una chiave a 56 bit.</span><span class="sxs-lookup"><span data-stu-id="78cde-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="78cde-123">Quando un'applicazione server richiede la riservatezza (qop = "auth-conf") Microsoft Digest genererà una richiesta di verifica che offre al client tutte le crittografie installate nel server e supportate da digest.</span><span class="sxs-lookup"><span data-stu-id="78cde-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="78cde-124">Il client digest selezionerà la crittografia più sicura disponibile.</span><span class="sxs-lookup"><span data-stu-id="78cde-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="78cde-125">Per informazioni dettagliate su come specificare la riservatezza, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="78cde-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
