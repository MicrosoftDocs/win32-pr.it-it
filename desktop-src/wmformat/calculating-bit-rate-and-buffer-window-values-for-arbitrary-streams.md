---
title: Calcolo della frequenza di bit e dei valori della finestra del buffer per le Flussi
description: Calcolo della frequenza di bit e dei valori della finestra del buffer per le Flussi
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flussi, velocità in bit
- codec, calcolo delle velocità in bit per flussi arbitrari
- velocità in bit, calcolo per flussi arbitrari
- flussi, calcolo delle velocità in bit per i flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c86a866536bbe2565a3bc44bbe9f40743db26d948555bc6ec8a11eb60d7aa4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434485"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calcolo della frequenza di bit e dei valori della finestra del buffer per le Flussi

Il calcolo della frequenza in bit corretta e della finestra del buffer per un tipo di flusso arbitrario non è un'operazione scientifica esatta. Un approccio semplice consiste nell'impostare la velocità in bit in modo che corrisponda alla dimensione del flusso divisa per la lunghezza, in secondi. Ad esempio, un flusso contenente un totale di 68000 bit di durata di 20 secondi potrebbe avere una velocità in bit di 3400 bit al secondo (68000 bit/20 secondi = 3400 bit al secondo).

Il problema di questa semplice tecnica di assegnazione della velocità in bit è che non prende in considerazione la distribuzione dei dati all'interno del flusso. Molti flussi arbitrari contengono grandi quantità di dati a intervalli lungo la sequenza temporale del file. I flussi di immagini, ad esempio, hanno campioni piuttosto grandi, ma in genere distanti alcuni secondi. La finestra del buffer deve essere impostata per garantire che non si verifica un overflow del buffer.

Per controllare la finestra del buffer, moltiplicare la velocità in bit (bit al secondo) per la finestra del buffer (in secondi) e dividere per 1000 per ottenere la dimensione, in bit, del buffer per il flusso. Assicurarsi quindi che le dimensioni del buffer siano sufficienti per contenere qualsiasi combinazione di campioni nel flusso inferiore alla finestra del buffer nel tempo di presentazione. In caso di dubbi, impostare entrambi i valori un po' più in alto di quanto si pensi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Buffering del contenuto**](buffering-content.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




