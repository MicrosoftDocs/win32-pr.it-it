---
description: Diverse funzioni aggiungono un contesto del certificato o un collegamento a un contesto a un \[ SDK (Software Development Kit) della piattaforma di archiviazione \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Utilizzo dei certificati negli archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347661"
---
# <a name="working-with-certificates-in-certificate-stores"></a><span data-ttu-id="0d0ff-103">Utilizzo dei certificati negli archivi certificati</span><span class="sxs-lookup"><span data-stu-id="0d0ff-103">Working with Certificates in Certificate Stores</span></span>

<span data-ttu-id="0d0ff-104">Diverse funzioni aggiungono un contesto di certificato o un collegamento a un contesto in un archivio.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-104">Several functions add a certificate context or a link to a context to a store.</span></span>

<span data-ttu-id="0d0ff-105">Per i certificati già presenti nel formato del contesto del certificato:</span><span class="sxs-lookup"><span data-stu-id="0d0ff-105">For certificates already in certificate context form:</span></span>

-   [<span data-ttu-id="0d0ff-106">**CertAddCertificateContextToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-106">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [<span data-ttu-id="0d0ff-107">**CertAddCRLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-107">**CertAddCRLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [<span data-ttu-id="0d0ff-108">**CertAddCTLContextToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-108">**CertAddCTLContextToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [<span data-ttu-id="0d0ff-109">**CertAddCertificateLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-109">**CertAddCertificateLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [<span data-ttu-id="0d0ff-110">**CertAddCRLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-110">**CertAddCRLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [<span data-ttu-id="0d0ff-111">**CertAddCTLLinkToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-111">**CertAddCTLLinkToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

<span data-ttu-id="0d0ff-112">Per i certificati con formato codificato ma non per i contesti di certificato completi:</span><span class="sxs-lookup"><span data-stu-id="0d0ff-112">For certificates that are in encoded form but not full certificate contexts:</span></span>

-   [<span data-ttu-id="0d0ff-113">**CertAddEncodedCertificateToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-113">**CertAddEncodedCertificateToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [<span data-ttu-id="0d0ff-114">**CertAddEncodedCRLToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-114">**CertAddEncodedCRLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [<span data-ttu-id="0d0ff-115">**CertAddEncodedCTLToStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-115">**CertAddEncodedCTLToStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

<span data-ttu-id="0d0ff-116">Le funzioni seguenti eliminano un certificato, un CRL o un elenco di scopi consentiti da un archivio diminuendo di uno il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-116">The following functions delete a certificate, CRL, or CTL from a store by decrementing its reference count by one.</span></span> <span data-ttu-id="0d0ff-117">Se il conteggio dei riferimenti diventa zero, viene liberata la memoria utilizzata per archiviare il certificato, l'elenco CRL o l'elenco di scopi consentiti.</span><span class="sxs-lookup"><span data-stu-id="0d0ff-117">If this causes the reference count to become zero, the memory used to store the certificate, CRL, or CTL is freed.</span></span>

-   [<span data-ttu-id="0d0ff-118">**CertDeleteCertificateFromStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-118">**CertDeleteCertificateFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [<span data-ttu-id="0d0ff-119">**CertDeleteCRLFromStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-119">**CertDeleteCRLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [<span data-ttu-id="0d0ff-120">**CertDeleteCTLFromStore**</span><span class="sxs-lookup"><span data-stu-id="0d0ff-120">**CertDeleteCTLFromStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



