---
title: Conversione di dati da un formato a un altro
description: Conversione di dati da un formato a un altro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- gestione compressione audio,conversione di dati
- ACM (Audio Compression Manager), conversione dei dati
- Esempi di ACM, conversione di dati
- conversione dei dati
- Funzione acmStreamOpen
- Funzione acmStreamSize
- Funzione acmStreamPrepareHeader
- Funzione acmStreamConvert
- Funzione acmStreamUnprepareHeader
- Funzione acmStreamClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ec1050066b92a356067085b491f5ddbf4bded47789c6e15a5187ea74c47c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144812"
---
# <a name="converting-data-from-one-format-to-another"></a>Conversione di dati da un formato a un altro

ACM usa funzioni di flusso per supportare la conversione del formato dati. I convertitori in ACM modificano il formato, ma non il tipo di dati. Ad esempio, un modulo convertitore può modificare i dati a 44 kHz, a 16 bit in dati a 44 kHz e a 8 bit.

Le funzioni ACM seguenti supportano la conversione del formato dati. Sono elencati nell'ordine in cui vengono in genere utilizzati.

-   La [**funzione acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) apre un flusso di conversione.
-   La [**funzione acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcola le dimensioni appropriate del buffer di origine o di destinazione.
-   La [**funzione acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara i buffer di origine e di destinazione da usare in una conversione.
-   La [**funzione acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) converte i dati in un buffer di origine nel formato di destinazione, scrivendo i dati convertiti nel buffer di destinazione.
-   La [**funzione acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) pulisce i buffer di origine e di destinazione preparati da **acmStreamPrepareHeader.** È necessario chiamare questa funzione prima di liberare i buffer di origine e di destinazione.
-   La [**funzione acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) chiude un flusso di conversione.

Durante la conversione dei dati, identificare innanzitutto il formato di origine, quindi scegliere il formato di destinazione. Il modo più semplice per eseguire questa operazione è usare la funzione [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) che visualizza una finestra di dialogo di selezione del formato e restituisce la scelta del formato dell'utente.

Quando si conoscono i formati di origine e di destinazione, è possibile usare [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) per aprire un flusso di conversione. È quindi possibile usare la [**funzione acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) per determinare le dimensioni del buffer appropriate.

Il passaggio successivo consiste nel preparare i buffer da usare nella conversione usando [**acmStreamPrepareHeader.**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)

Per eseguire la conversione, [**usare acmStreamConvert fino**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) a quando non sono stati elaborati tutti i buffer. Al termine della conversione, usare [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) per pulire i buffer e quindi [**usare acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) per chiudere il flusso di conversione.

 

 




