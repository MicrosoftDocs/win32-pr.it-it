---
description: In un'infrastruttura a chiave pubblica Microsoft, le richieste di certificati vengono inviate da computer client alle autorità di certificazione (CAs) come stringa binaria che contiene una sequenza di strutture di dati codificate.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codifica della richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756545"
---
# <a name="certificate-request-encoding"></a>Codifica della richiesta di certificato

In un'infrastruttura a chiave pubblica Microsoft, le richieste di certificati vengono inviate da computer client alle autorità di certificazione (CAs) come stringa binaria che contiene una sequenza di strutture di dati codificate. L'API di registrazione certificati usa la sintassi astratta One (ASN. 1) per descrivere e codificare queste strutture. Ai fini di questa documentazione, ASN. 1 può essere concettualmente suddiviso nelle regole di sintassi (ISO 8824) che descrivono le strutture dei dati e le regole di codifica (ISO 8825) che specificano la modalità di codifica dei dati per la trasmissione di rete. Per altre informazioni, vedere i seguenti argomenti:

-   [Introduzione alla sintassi e alla codifica ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Sistema di tipi ASN. 1](about-asn-1-type-system.md)
-   [Distinguished Encoding Rules](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



