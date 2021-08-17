---
description: In un'infrastruttura a chiave pubblica (PKI) Microsoft le richieste di certificato vengono inviate dai computer client alle autorità di certificazione (CA) come stringa binaria che contiene una sequenza di strutture di dati codificati.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codifica delle richieste di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6bb65b496264fcd1f9667416c78d5d8cf246f1c9aa4cf736990a1f61669f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904850"
---
# <a name="certificate-request-encoding"></a>Codifica delle richieste di certificato

In un'infrastruttura a chiave pubblica (PKI) Microsoft le richieste di certificato vengono inviate dai computer client alle autorità di certificazione (CA) come stringa binaria che contiene una sequenza di strutture di dati codificati. L'API di registrazione certificati usa Abstract Syntax Notation One (ASN.1) per descrivere e codificare queste strutture. Ai fini di questa documentazione, è possibile suddividere concettualmente ASN.1 nelle regole di sintassi (ISO 8824) che descrivono le strutture dei dati e le regole di codifica (ISO 8825) che specificano come codificare i dati per la trasmissione di rete. Per altre informazioni, vedere i seguenti argomenti:

-   [Introduzione alla sintassi e alla codifica ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Sistema di tipi ASN.1](about-asn-1-type-system.md)
-   [Distinguished Encoding Rules](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



