---
title: Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari
description: Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flussi, velocità in bit
- codec, calcolo della velocità in bit per flussi arbitrari
- velocità in bit, calcolo per flussi arbitrari
- flussi, calcolo di velocità in bit per flussi arbitrari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044140"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calcolo dei valori della velocità in bit e della finestra del buffer per flussi arbitrari

Il calcolo della velocità in bit e della finestra del buffer appropriate per un tipo di flusso arbitrario non è una scienza esatta. Un approccio semplice consiste nell'impostare la velocità in bit in modo che corrisponda alla dimensione del flusso divisa per la relativa lunghezza, in secondi. Ad esempio, un flusso contenente un totale di 68000 bit che dura 20 secondi potrebbe avere una velocità in bit di 3400 bit al secondo (68000 bit/20 secondi = 3400 bit al secondo).

Il problema di questa semplice tecnica di assegnazione della velocità in bit è che non prende in considerazione la distribuzione dei dati all'interno del flusso. Molti flussi arbitrari contengono maggiori quantità di dati a intervalli lungo la sequenza temporale del file. I flussi di immagini, ad esempio, presentano esempi di dimensioni piuttosto elevate, ma sono in genere separati da pochi secondi. È necessario impostare la finestra buffer per verificare che il buffer non venga overflow.

Per controllare la finestra del buffer, moltiplicare la velocità in bit (bit al secondo) con la finestra del buffer (in secondi) e dividere per 1000 per ottenere la dimensione, in bit, del buffer per il flusso. Assicurarsi quindi che le dimensioni del buffer siano sufficienti a mantenere una qualsiasi combinazione di campioni nel flusso inferiore alla finestra del buffer in fase di presentazione. In caso di dubbi, impostare entrambi i valori su un valore leggermente superiore rispetto a quelli necessari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Contenuto del buffer**](buffering-content.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




