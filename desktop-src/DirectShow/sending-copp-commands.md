---
description: Invio di comandi COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Invio di comandi COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66a6ad66abe7e6c4a596446b147fe5943c5460b4ef540dbc5e5a3dfad4bdc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078881"
---
# <a name="sending-copp-commands"></a>Invio di comandi COPP

Per inviare un comando COPP (Certified Output Protection Protocol), compilare una [**struttura AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) come segue:

-   **guidCommandID**. GUID che identifica il comando. Vedere le informazioni di riferimento sul comando COPP.
-   **dwSequence**. Numero di sequenza del comando. Incrementare questo valore dopo ogni comando. Questo valore viene visualizzato come **uCommandSeq** in [Avvio di una sessione COPP.](initiating-a-copp-session.md)
-   **cbSizeData**. Dimensione, in byte, dei dati necessari per il comando.
-   **CommandData**. Dati per il comando.

Dopo aver compilato questi dati, calcolare il MAC per il comando:

1.  Calcolare il tag OMAC-1 per il blocco di dati visualizzato dopo il membro **macKDI** della **struttura AMCOPPCommand.**
2.  Copiare questo valore nel **membro macKDI** della struttura .

Passare ora la struttura al [**metodo IAMCertifiedOutputProtection::P rotectionCommand.**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



