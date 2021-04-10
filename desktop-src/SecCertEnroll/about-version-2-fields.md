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
# <a name="version-2-fields"></a>Campi versione 2

I certificati X.509 versione 2 contengono i campi di base definiti nella versione 1 più i campi seguenti.

## <a name="issuer-unique-identifier"></a>Identificatore univoco dell'autorità di certificazione

Contiene un valore univoco che può essere usato per rendere non ambiguo il nome X.500 dell'autorità di certificazione se riutilizzato da diverse entità nel tempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Identificatore univoco del soggetto

Contiene un valore univoco che può essere usato per rendere non ambiguo il nome X.500 del soggetto del certificato se riutilizzato da diverse entità nel tempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Campi di base](about-basic-fields.md)
</dt> <dt>

[Estensioni versione 3](about-version-3-extensions.md)
</dt> <dt>

[Certificati di chiave pubblica X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



