---
description: Ai certificati sono associate proprietà, ad esempio il nome visualizzato, la descrizione e gli utilizzi consentiti, che possono essere visualizzati e modificati.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Creazione, visualizzazione e gestione dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306465"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="7555f-103">Creazione, visualizzazione e gestione dei certificati</span><span class="sxs-lookup"><span data-stu-id="7555f-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="7555f-104">I [*certificati*](../secgloss/c-gly.md) sono strutture di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7555f-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="7555f-105">Il contenuto di un certificato può essere visualizzato ma non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="7555f-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="7555f-106">Le informazioni nel certificato stesso includono le date di validità del certificato, l'emittente, l'oggetto e la chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="7555f-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="7555f-107">Tuttavia, i certificati hanno proprietà associate, ad esempio un nome visualizzato, una descrizione e gli utilizzi consentiti, che possono essere visualizzati e modificati.</span><span class="sxs-lookup"><span data-stu-id="7555f-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="7555f-108">Questa sezione illustra la creazione di certificati di test, la visualizzazione di certificati e la gestione di certificati e altri oggetti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7555f-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="7555f-109">I certificati e i [*certificati di autore del software*](../secgloss/s-gly.md) (SPCs) che possono essere creati con Makecert sono rigorosamente a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="7555f-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="7555f-110">Un [*certificato radice*](../secgloss/r-gly.md) di test e una [*chiave privata*](../secgloss/p-gly.md) radice test sono forniti solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="7555f-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="7555f-111">I fornitori di software indipendenti devono ottenere un certificato da GTE, VeriSign, Inc. o da un'altra [*autorità di certificazione*](../secgloss/c-gly.md) (CA) per firmare il codice che verrà distribuito al pubblico.</span><span class="sxs-lookup"><span data-stu-id="7555f-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="7555f-112">Questa sezione include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7555f-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="7555f-113">Uso di MakeCert</span><span class="sxs-lookup"><span data-stu-id="7555f-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="7555f-114">Uso di Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="7555f-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="7555f-115">Utilizzo di CertMgr</span><span class="sxs-lookup"><span data-stu-id="7555f-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
