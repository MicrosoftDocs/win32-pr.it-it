---
description: Una catena di certificati è una raccolta gerarchica di certificati che conduce dall'utente finale o dal computer a una radice di attendibilità, in genere l'autorità di certificazione radice (CA) di un'organizzazione.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Catena di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319383"
---
# <a name="certificate-chain"></a><span data-ttu-id="f76e3-103">Catena di certificati</span><span class="sxs-lookup"><span data-stu-id="f76e3-103">Certificate Chain</span></span>

<span data-ttu-id="f76e3-104">Una catena di certificati è una raccolta gerarchica di certificati che conduce dall'utente finale o dal computer a una radice di attendibilità, in genere l'autorità di certificazione radice (CA) di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f76e3-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="f76e3-105">Poiché tutte le entità considerano presumibilmente attendibile il certificato radice, un'entità può ottenere l'attendibilità in un certificato dell'entità finale verificando la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="f76e3-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="f76e3-106">Per la verifica in genere è necessario stabilire che ogni certificato nella catena:</span><span class="sxs-lookup"><span data-stu-id="f76e3-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="f76e3-107">Viene firmato dalla chiave pubblica nel certificato precedente.</span><span class="sxs-lookup"><span data-stu-id="f76e3-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="f76e3-108">Non è scaduto.</span><span class="sxs-lookup"><span data-stu-id="f76e3-108">Has not expired.</span></span>
-   <span data-ttu-id="f76e3-109">Non è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="f76e3-109">Has not been revoked.</span></span>
-   <span data-ttu-id="f76e3-110">È conforme ai criteri specificati dai certificati precedenti.</span><span class="sxs-lookup"><span data-stu-id="f76e3-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f76e3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f76e3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f76e3-112">Gerarchia di certificati</span><span class="sxs-lookup"><span data-stu-id="f76e3-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="f76e3-113">Certificazione incrociata</span><span class="sxs-lookup"><span data-stu-id="f76e3-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="f76e3-114">Modelli di attendibilità</span><span class="sxs-lookup"><span data-stu-id="f76e3-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



