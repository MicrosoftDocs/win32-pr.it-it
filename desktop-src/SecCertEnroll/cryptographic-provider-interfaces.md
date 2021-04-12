---
description: Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider di servizi di crittografia.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Interfacce del provider del crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129887"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="8b35c-103">Interfacce del provider del crittografia</span><span class="sxs-lookup"><span data-stu-id="8b35c-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="8b35c-104">Le interfacce seguenti possono essere utilizzate per recuperare informazioni sui provider di servizi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="8b35c-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="8b35c-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8b35c-105">Interface</span></span>                                    | <span data-ttu-id="8b35c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b35c-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="8b35c-107">**ICspAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="8b35c-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="8b35c-108">Rappresenta un algoritmo implementato da un provider del crittografia.</span><span class="sxs-lookup"><span data-stu-id="8b35c-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="8b35c-109">**ICspAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="8b35c-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="8b35c-110">Gestisce una raccolta di oggetti [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="8b35c-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="8b35c-111">**ICspInformation**</span><span class="sxs-lookup"><span data-stu-id="8b35c-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="8b35c-112">Consente di accedere alle informazioni generali su un provider di servizi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="8b35c-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="8b35c-113">**ICspInformations**</span><span class="sxs-lookup"><span data-stu-id="8b35c-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="8b35c-114">Gestisce una raccolta di oggetti [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) .</span><span class="sxs-lookup"><span data-stu-id="8b35c-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="8b35c-115">**ICspStatus**</span><span class="sxs-lookup"><span data-stu-id="8b35c-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="8b35c-116">Contiene informazioni su una coppia di provider/algoritmi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="8b35c-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="8b35c-117">**ICspStatuses**</span><span class="sxs-lookup"><span data-stu-id="8b35c-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="8b35c-118">Gestisce una raccolta di oggetti [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) .</span><span class="sxs-lookup"><span data-stu-id="8b35c-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="8b35c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b35c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b35c-120">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="8b35c-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



