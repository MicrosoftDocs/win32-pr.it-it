---
description: Abstract Syntax Notation One (ASN.1) definisce i set di regole seguenti che regolano la modalità di codifica e decodifica delle strutture di dati inviate tra computer.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d592fdfbb2532f5c718aadaaf32e63f352ed6ab427e9908465fcb5998839f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883071"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

Abstract Syntax Notation One (ASN.1) definisce i set di regole seguenti che regolano la modalità di codifica e decodifica delle strutture di dati inviate tra computer.

-   Regole di codifica di base (BER)
-   Regole di codifica canonica (CER)
-   Distinguished Encoding Rules (DER)
-   Regole di codifica con pacchetto (PER)

Il set di regole originale è stato definito dalla specifica BER. CER e DER sono stati sviluppati in seguito come subset specializzati di BER. PER è stato sviluppato in risposta a critiche sulla quantità di larghezza di banda necessaria per trasmettere i dati usando BER o le relative varianti. PER offre un risparmio significativo.

DER è stato creato per soddisfare i requisiti della specifica X.509 per il trasferimento sicuro dei dati. L'API di registrazione certificati usa esclusivamente DER. Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Sintassi di trasferimento DER](about-der-transfer-syntax.md)
-   [Codifica DER dei tipi ASN.1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistema di tipi ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codifica delle richieste di certificato](about-certificate-request-encoding.md)
</dt> <dt>

[Introduzione alla sintassi e alla codifica ASN.1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



