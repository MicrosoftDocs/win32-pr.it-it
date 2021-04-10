---
description: I certificati X.509 versione 2 contengono i campi di base definiti nella versione 1 più i campi seguenti.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Campi versione 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225867"
---
# <a name="version-2-fields"></a><span data-ttu-id="784af-103">Campi versione 2</span><span class="sxs-lookup"><span data-stu-id="784af-103">Version 2 Fields</span></span>

<span data-ttu-id="784af-104">I certificati X.509 versione 2 contengono i campi di base definiti nella versione 1 più i campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="784af-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="784af-105">Identificatore univoco dell'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="784af-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="784af-106">Contiene un valore univoco che può essere usato per rendere non ambiguo il nome X.500 dell'autorità di certificazione se riutilizzato da diverse entità nel tempo.</span><span class="sxs-lookup"><span data-stu-id="784af-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="784af-107">Identificatore univoco del soggetto</span><span class="sxs-lookup"><span data-stu-id="784af-107">Subject Unique Identifier</span></span>

<span data-ttu-id="784af-108">Contiene un valore univoco che può essere usato per rendere non ambiguo il nome X.500 del soggetto del certificato se riutilizzato da diverse entità nel tempo.</span><span class="sxs-lookup"><span data-stu-id="784af-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="784af-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="784af-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="784af-110">Campi di base</span><span class="sxs-lookup"><span data-stu-id="784af-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="784af-111">Estensioni versione 3</span><span class="sxs-lookup"><span data-stu-id="784af-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="784af-112">Certificati di chiave pubblica X. 509</span><span class="sxs-lookup"><span data-stu-id="784af-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



