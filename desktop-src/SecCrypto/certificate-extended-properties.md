---
description: I dati in un certificato, un elenco di revoche di certificati (CRL) o un contesto elenco certificati attendibili (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Proprietà estese del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131051"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="2d10a-103">Proprietà estese del certificato</span><span class="sxs-lookup"><span data-stu-id="2d10a-103">Certificate Extended Properties</span></span>

<span data-ttu-id="2d10a-104">I dati in un [*certificato*](../secgloss/c-gly.md), un [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL) o un [*contesto*](../secgloss/c-gly.md) [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL), incluse eventuali estensioni, sono di sola lettura e non possono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="2d10a-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="2d10a-105">Tuttavia, sulle piattaforme Microsoft, i certificati CryptoAPI hanno anche proprietà estese dinamiche che possono essere aggiunte e modificate.</span><span class="sxs-lookup"><span data-stu-id="2d10a-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="2d10a-106">Le proprietà estese sono associate a un certificato e non fanno parte di un certificato emesso da un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="2d10a-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="2d10a-107">Le proprietà estese non sono disponibili in un certificato quando viene usato in una piattaforma non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2d10a-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="2d10a-108">Queste proprietà includono i dati che:</span><span class="sxs-lookup"><span data-stu-id="2d10a-108">These properties include data that:</span></span>

-   <span data-ttu-id="2d10a-109">Si riferisce alla chiave privata da usare con il certificato.</span><span class="sxs-lookup"><span data-stu-id="2d10a-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="2d10a-110">Indica il tipo di hash da eseguire sul certificato.</span><span class="sxs-lookup"><span data-stu-id="2d10a-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="2d10a-111">Fornisce informazioni definite dall'utente associate al certificato.</span><span class="sxs-lookup"><span data-stu-id="2d10a-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="2d10a-112">Sulle piattaforme Microsoft, i valori di queste proprietà vengono collegati e spostati con il certificato.</span><span class="sxs-lookup"><span data-stu-id="2d10a-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="2d10a-113">Le proprietà attualmente predefinite identificate con ID proprietà includono le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d10a-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="2d10a-114">Queste proprietà legano un certificato a un particolare CSP e, all'interno di tale CSP, a una chiave privata specifica:</span><span class="sxs-lookup"><span data-stu-id="2d10a-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="2d10a-115">\_ \_ \_ ID Prop dell'handle \_ della chiave CERT \_</span><span class="sxs-lookup"><span data-stu-id="2d10a-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="2d10a-116">\_ID di \_ attestazione della chiave \_ CERT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2d10a-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="2d10a-117">\_ \_ ID Prop del contesto della chiave CERT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2d10a-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="2d10a-118">Queste proprietà indicano l'algoritmo hash da usare quando viene eseguita un'operazione di hashing:</span><span class="sxs-lookup"><span data-stu-id="2d10a-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="2d10a-119">\_ID proprietà \_ hash \_ SHA1 \_ CERT</span><span class="sxs-lookup"><span data-stu-id="2d10a-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="2d10a-120">\_ID della \_ prop di hash MD5 \_ CERT \_</span><span class="sxs-lookup"><span data-stu-id="2d10a-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="2d10a-121">Per gli elenchi completi delle proprietà del certificato esteso attualmente definite e delle descrizioni del significato e dell'uso di ogni proprietà, vedere [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span><span class="sxs-lookup"><span data-stu-id="2d10a-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d10a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d10a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d10a-123">**CertGetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="2d10a-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="2d10a-124">**CertGetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="2d10a-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="2d10a-125">**CertSetCRLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="2d10a-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="2d10a-126">**CertSetCTLContextProperty**</span><span class="sxs-lookup"><span data-stu-id="2d10a-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
