---
description: Le funzioni CertAddCertificateLinkToStore, CertAddCRLLinkToStore e CertAddCTLLinkToStore aggiungono collegamenti a contesti esistenti in archivi certificati anziché aggiungere copie di tali contesti.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Collegamenti al certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131446"
---
# <a name="certificate-links"></a><span data-ttu-id="ab9ec-103">Collegamenti al certificato</span><span class="sxs-lookup"><span data-stu-id="ab9ec-103">Certificate Links</span></span>

<span data-ttu-id="ab9ec-104">Le funzioni [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)e [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) aggiungono collegamenti a contesti esistenti in [*archivi certificati*](../secgloss/c-gly.md) anziché aggiungere copie di tali contesti.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-104">The functions [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore), and [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) add links to existing contexts into [*certificate stores*](../secgloss/c-gly.md) rather than adding copies of those contexts.</span></span> <span data-ttu-id="ab9ec-105">L'aggiunta di collegamenti agli archivi rende disponibile lo stesso [*certificato*](../secgloss/c-gly.md)fisico, [*CRL*](../secgloss/c-gly.md)o [*CTL*](../secgloss/c-gly.md) tramite diversi archivi.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-105">Adding links to stores makes the same physical [*certificate*](../secgloss/c-gly.md), [*CRL*](../secgloss/c-gly.md), or [*CTL*](../secgloss/c-gly.md) available through several different stores.</span></span> <span data-ttu-id="ab9ec-106">Le modifiche apportate alle proprietà estese di un [*contesto*](../secgloss/c-gly.md) dall'archivio del contesto originale o da un archivio in cui è archiviato un collegamento a tale contesto sono disponibili nell'archivio che contiene il contesto originale e in tutti gli altri archivi che contengono collegamenti a tale contesto.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-106">Changes made to the extended properties of a [*context*](../secgloss/c-gly.md) from the store of the original context, or from a store where a link to that context is stored, are available in the store that holds the original context and in all other stores that have links to that context.</span></span>

<span data-ttu-id="ab9ec-107">Per un esempio in cui viene usato [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), vedere il [programma C di esempio: operazioni sull'archivio certificati](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ab9ec-107">For an example that uses [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

![collegamenti al certificato](images/mancert1.png)

<span data-ttu-id="ab9ec-109">Si supponga che i certificati A. 1, A. 2, A. 3 e A. 4 siano originariamente nel negozio A e che i certificati B. 1, B. 2, B. 3 e B. 4 siano originariamente inclusi nello Store B.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-109">Assume that certificates A.1, A.2, A.3, and A.4 are originally in store A, and certificates B.1, B.2, B.3, and B.4 are originally in store B.</span></span>

-   <span data-ttu-id="ab9ec-110">Il diagramma mostra un collegamento aggiunto nell'archivio B al certificato A. 2 e un collegamento aggiunto nell'archivio a al certificato B. 2.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-110">The diagram shows a link added in store B to certificate A.2 and a link added in store A to certificate B.2.</span></span>
-   <span data-ttu-id="ab9ec-111">L'originale del certificato A. 2 è ancora nell'archivio A. L'originale di B. 2 è ancora nell'archivio B.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-111">The original of certificate A.2 is still in store A. The original of B.2 is still in store B.</span></span>
-   <span data-ttu-id="ab9ec-112">Tutte le modifiche apportate alle proprietà estese del certificato A. 2 o del certificato B. 2 dall'archivio A o dall'archivio B saranno disponibili per entrambi i punti vendita.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-112">Any changes made to the extended properties of certificate A.2 or certificate B.2 from either store A or store B will be available to both stores.</span></span>
-   <span data-ttu-id="ab9ec-113">Se una copia del certificato A. 3 è stata effettuata e archiviata nell'archivio B, qualsiasi modifica apportata alle proprietà estese del certificato originale A. 3 creato dall'archivio A non sarà visibile nella nuova copia nell'archivio B. Se sono state apportate modifiche alle proprietà estese della copia del certificato A. 3 nell'archivio B, tali modifiche non influiranno sul contenuto del certificato originale A. 3 e non saranno visibili dall'archivio A.</span><span class="sxs-lookup"><span data-stu-id="ab9ec-113">If a copy of certificate A.3 were made and stored in store B, any changes to the extended properties of the original A.3 certificate made from store A would not be visible in the new copy in store B. If changes were made to the extended properties of the copy of certificate A.3 in store B, those changes would not affect the contents of the original A.3 certificate and would not be visible from store A.</span></span>

 

 
