---
title: Conversione di dati da un formato a un altro
description: Conversione di dati da un formato a un altro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gestione compressione audio (ACM), conversione dei dati
- ACM (Gestione compressione audio), conversione dei dati
- Esempi di ACM, conversione di dati
- conversione dei dati
- acmStreamOpen (funzione)
- acmStreamSize (funzione)
- acmStreamPrepareHeader (funzione)
- acmStreamConvert (funzione)
- acmStreamUnprepareHeader (funzione)
- acmStreamClose (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329756"
---
# <a name="converting-data-from-one-format-to-another"></a>Conversione di dati da un formato a un altro

L'ACM usa le funzioni di flusso per supportare la conversione del formato dati. I convertitori nell'ACM cambiano il formato, ma non il tipo di dati. Un modulo Converter, ad esempio, può modificare 44-kHz, dati a 16 bit in dati a 8 bit a 44-kHz.

Le funzioni ACM seguenti supportano la conversione del formato dati. Sono elencate nell'ordine in cui vengono in genere usate.

-   La funzione [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) apre un flusso di conversione.
-   La funzione [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcola la dimensione appropriata del buffer di origine o di destinazione.
-   La funzione [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara i buffer di origine e di destinazione da utilizzare in una conversione.
-   La funzione [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) converte i dati in un buffer di origine nel formato di destinazione, scrivendo i dati convertiti nel buffer di destinazione.
-   La funzione [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) pulisce i buffer di origine e di destinazione preparati da **acmStreamPrepareHeader**. È necessario chiamare questa funzione prima di liberare i buffer di origine e di destinazione.
-   La funzione [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) chiude un flusso di conversione.

Quando si convertono i dati, identificare prima il formato di origine, quindi scegliere il formato di destinazione. Il modo più semplice per eseguire questa operazione consiste nell'usare la funzione [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , che visualizza una finestra di dialogo di selezione del formato e restituisce la scelta del formato dell'utente.

Quando si conoscono i formati di origine e di destinazione, è possibile usare [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) per aprire un flusso di conversione. È quindi possibile usare la funzione [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) per determinare le dimensioni del buffer appropriate.

Il passaggio successivo consiste nel preparare i buffer da usare nella conversione usando [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).

Per eseguire la conversione, utilizzare [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) fino a quando non vengono elaborati tutti i buffer. Al termine della conversione, usare [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) per pulire i buffer e quindi usare [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) per chiudere il flusso di conversione.

 

 




