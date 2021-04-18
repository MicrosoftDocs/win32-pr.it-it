---
description: Invio di comandi COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Invio di comandi COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303873"
---
# <a name="sending-copp-commands"></a>Invio di comandi COPP

Per inviare un comando COPP (Certified Output Protocol), compilare una struttura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) come indicato di seguito:

-   **guidCommandID**. GUID che identifica il comando. Vedere le informazioni di riferimento sui comandi di COPP.
-   **dwSequence**. Numero di sequenza del comando. Incrementare questo valore dopo ogni comando. Questo valore viene visualizzato come **uCommandSeq** durante [l'avvio di una sessione COPP](initiating-a-copp-session.md).
-   **cbSizeData**. Dimensione, in byte, dei dati necessari per il comando.
-   **CommandData**. Dati per il comando.

Dopo aver compilato i dati, calcolare il MAC per il comando:

1.  Calcolare il tag OMAC-1 per il blocco di dati visualizzato dopo il membro **macKDI** della struttura **AMCOPPCommand** .
2.  Copiare questo valore nel membro **macKDI** della struttura.

Passare quindi la struttura al metodo [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



