---
description: Le funzioni di integrità dell'immagine gestiscono il set di certificati in un file di immagine.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funzioni di integrità immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049166"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="322bf-103">Funzioni di integrità immagini</span><span class="sxs-lookup"><span data-stu-id="322bf-103">Image Integrity Functions</span></span>

<span data-ttu-id="322bf-104">Le funzioni di integrità dell'immagine gestiscono il set di certificati in un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="322bf-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="322bf-105">Vengono fornite routine per aggiungere, rimuovere ed eseguire query sui certificati.</span><span class="sxs-lookup"><span data-stu-id="322bf-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="322bf-106">È disponibile anche una funzione per ottenere il flusso di byte di un file di immagine necessario per calcolare un digest del messaggio del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="322bf-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="322bf-107">Questa operazione è necessaria per creare certificati di firma.</span><span class="sxs-lookup"><span data-stu-id="322bf-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="322bf-108">Ogni certificato in un file dispone di un indice che può essere modificato quando vengono rimossi i certificati.</span><span class="sxs-lookup"><span data-stu-id="322bf-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="322bf-109">I nuovi certificati verranno sempre aggiunti "alla fine" dell'elenco dei certificati esistenti.</span><span class="sxs-lookup"><span data-stu-id="322bf-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="322bf-110">Ovvero verranno assegnati indici che sono maggiori di tutti gli indici attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="322bf-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="322bf-111">In generale, un'applicazione non deve presupporre che un determinato certificato abbia lo stesso indice con l'ultima volta in cui è stato fatto riferimento.</span><span class="sxs-lookup"><span data-stu-id="322bf-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="322bf-112">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="322bf-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="322bf-113">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="322bf-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="322bf-114">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="322bf-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="322bf-115">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="322bf-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="322bf-116">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="322bf-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="322bf-117">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="322bf-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="322bf-118">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="322bf-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



