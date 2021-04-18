---
description: Le interfacce di utilizzo generali seguenti sono supportate dall'API di registrazione del certificato.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfacce Helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316716"
---
# <a name="helper-interfaces"></a><span data-ttu-id="7ca0d-103">Interfacce Helper</span><span class="sxs-lookup"><span data-stu-id="7ca0d-103">Helper Interfaces</span></span>

<span data-ttu-id="7ca0d-104">Le interfacce di utilizzo generali seguenti sono supportate dall'API di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="7ca0d-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="7ca0d-105">Interface</span></span>                                                                    | <span data-ttu-id="7ca0d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ca0d-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ca0d-107">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="7ca0d-108">Crea una stringa con codifica Unicode da una matrice di byte, crea una matrice di byte da una stringa con codifica Unicode e modifica il tipo di codifica Unicode applicato a una stringa.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="7ca0d-109">**ICertificateAttestationChallenge**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="7ca0d-110">Supporta le richieste di attestazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="7ca0d-111">**IObjectId**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="7ca0d-112">Rappresenta un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="7ca0d-113">**IObjectIds**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="7ca0d-114">Gestisce una raccolta di oggetti [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .</span><span class="sxs-lookup"><span data-stu-id="7ca0d-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="7ca0d-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="7ca0d-116">Rappresenta un nome distinto X. 500.</span><span class="sxs-lookup"><span data-stu-id="7ca0d-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="7ca0d-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="7ca0d-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="7ca0d-118">Interfaccia della chiave di verifica dell'autenticità X. 509</span><span class="sxs-lookup"><span data-stu-id="7ca0d-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7ca0d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ca0d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca0d-120">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="7ca0d-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



