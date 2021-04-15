---
description: Abstract Syntax Notation One (ASN. 1) definisce i set di regole seguenti che determinano il modo in cui le strutture dei dati inviate tra i computer vengono codificate e decodificate.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527001"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

Abstract Syntax Notation One (ASN. 1) definisce i set di regole seguenti che determinano il modo in cui le strutture dei dati inviate tra i computer vengono codificate e decodificate.

-   Regole di codifica di base (BER)
-   Regole di codifica canoniche (CER)
-   Distinguished Encoding Rules (DER)
-   Regole di codifica compresse (PER)

Il set di regole originale è stato definito dalla specifica BER. CER e DER sono stati sviluppati in seguito come subset specializzati di BER. PER è stato sviluppato in risposta a critiche sulla quantità di larghezza di banda necessaria per trasmettere i dati utilizzando BER o le relative varianti. PER fornisce un notevole risparmio.

DER è stato creato per soddisfare i requisiti della specifica X. 509 per il trasferimento sicuro dei dati. L'API di registrazione certificati usa esclusivamente DER. Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Sintassi di trasferimento DER](about-der-transfer-syntax.md)
-   [Codifica DER dei tipi ASN. 1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica della richiesta di certificato](about-certificate-request-encoding.md)
</dt> <dt>

[Introduzione alla sintassi e alla codifica ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



