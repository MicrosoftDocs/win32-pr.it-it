---
description: Le interfacce seguenti possono essere utilizzate per gestire le firme dei certificati e le chiavi pubbliche e private.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Firma del certificato e interfacce chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883314"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="8a55c-103">Firma del certificato e interfacce chiave</span><span class="sxs-lookup"><span data-stu-id="8a55c-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="8a55c-104">Le interfacce seguenti possono essere utilizzate per gestire le firme dei certificati e le chiavi pubbliche e private.</span><span class="sxs-lookup"><span data-stu-id="8a55c-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="8a55c-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8a55c-105">Interface</span></span>                                                      | <span data-ttu-id="8a55c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a55c-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a55c-107">**ISignerCertificate**</span><span class="sxs-lookup"><span data-stu-id="8a55c-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="8a55c-108">Rappresenta un certificato di firma che consente di firmare una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a55c-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="8a55c-109">**ISignerCertificates**</span><span class="sxs-lookup"><span data-stu-id="8a55c-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="8a55c-110">Gestisce una raccolta di oggetti [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .</span><span class="sxs-lookup"><span data-stu-id="8a55c-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="8a55c-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="8a55c-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="8a55c-112">Rappresenta una chiave privata asimmetrica che può essere utilizzata per la crittografia, la firma e il contratto di chiave.</span><span class="sxs-lookup"><span data-stu-id="8a55c-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="8a55c-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="8a55c-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="8a55c-114">Rappresenta una chiave pubblica in una coppia di chiavi pubblica/privata.</span><span class="sxs-lookup"><span data-stu-id="8a55c-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="8a55c-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="8a55c-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="8a55c-116">Rappresenta le informazioni utilizzate per firmare una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a55c-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="8a55c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a55c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a55c-118">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="8a55c-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



