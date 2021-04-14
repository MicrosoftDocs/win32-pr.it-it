---
description: Man mano che il numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI) aumenta, può diventare difficile per una singola autorità di certificazione (CA) rilevare efficacemente i certificati emessi.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Gerarchia di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552359"
---
# <a name="certificate-hierarchy"></a><span data-ttu-id="321a3-103">Gerarchia di certificati</span><span class="sxs-lookup"><span data-stu-id="321a3-103">Certificate Hierarchy</span></span>

<span data-ttu-id="321a3-104">Man mano che il numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI) aumenta, può diventare difficile per una singola autorità di certificazione (CA) rilevare efficacemente i certificati emessi.</span><span class="sxs-lookup"><span data-stu-id="321a3-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="321a3-105">Un modo per risolvere questo problema consiste nel creare una gerarchia di certificati in cui la CA delega l'autorità per emettere certificati alle autorità subordinate che possono, a loro volta, delegare l'autorità ai subordinati.</span><span class="sxs-lookup"><span data-stu-id="321a3-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="321a3-106">Ogni autorità di certificazione delega l'autorità emettendo un certificato CA a un subordinato.</span><span class="sxs-lookup"><span data-stu-id="321a3-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="321a3-107">La CA iniziale nella catena è denominata radice e non è necessario che un'entità stabilisca una relazione di trust con un'autorità di certificazione che risiede in una [catena di certificati](about-certificate-chain.md) diversa da quella in cui risiede l'entità.</span><span class="sxs-lookup"><span data-stu-id="321a3-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="321a3-108">Nella figura seguente viene illustrata una gerarchia di certificati costituita da una CA radice, due CA subordinata alla radice (una per il reparto marketing e una per il reparto produzione) e le autorità di certificazione subordinate.</span><span class="sxs-lookup"><span data-stu-id="321a3-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![diagramma gerarchia certificati](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="321a3-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="321a3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="321a3-111">Modelli di attendibilità</span><span class="sxs-lookup"><span data-stu-id="321a3-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



