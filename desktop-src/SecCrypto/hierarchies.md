---
description: Servizi certificati supporta le gerarchie di autorità di certificazione (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Gerarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316152"
---
# <a name="hierarchies"></a><span data-ttu-id="c498d-103">Gerarchie</span><span class="sxs-lookup"><span data-stu-id="c498d-103">Hierarchies</span></span>

<span data-ttu-id="c498d-104">Servizi certificati supporta le gerarchie di [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="c498d-104">Certificate Services supports [*certification authority*](../secgloss/c-gly.md) (CA) hierarchies.</span></span> <span data-ttu-id="c498d-105">Una [*gerarchia di CA*](../secgloss/c-gly.md) è costituita da una CA di primo livello (denominata CA radice) con una o più CA subordinate che sono state rilasciate certificati dalla CA radice.</span><span class="sxs-lookup"><span data-stu-id="c498d-105">A [*CA hierarchy*](../secgloss/c-gly.md) consists of a top-level CA (called the Root CA) with one or more subordinate CAs which have been issued certificates by the root CA.</span></span> <span data-ttu-id="c498d-106">Un possibile scenario della gerarchia CA si trova in un'organizzazione con una CA radice, che è stata usata per emettere certificati per diverse CA subordinate.</span><span class="sxs-lookup"><span data-stu-id="c498d-106">A possible CA hierarchy scenario would be in an organization with one root CA, which was used to issue certificates to several subordinate CAs.</span></span> <span data-ttu-id="c498d-107">Le CA subordinate possono quindi rilasciare i certificati dell'entità finale, ad esempio i certificati emessi a un utente.</span><span class="sxs-lookup"><span data-stu-id="c498d-107">The subordinate CAs can then issue end-entity certificates, such as certificates issued to a user.</span></span> <span data-ttu-id="c498d-108">Il certificato dell'utente conterrà un percorso di trust per la gerarchia di CA, in questo caso, incluso il certificato per la CA subordinata emittente e la CA radice.</span><span class="sxs-lookup"><span data-stu-id="c498d-108">The user's certificate will contain a trust path for the CA hierarchy, in this case, including the certificate for both the issuing subordinate CA as well as the root CA.</span></span>

 

 
