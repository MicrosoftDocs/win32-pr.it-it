---
title: Modelli di dati astratti
description: Ogni applicazione e ogni sistema operativo ha un modello di dati astratto.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- modelli di dati astratti programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298527"
---
# <a name="abstract-data-models"></a>Modelli di dati astratti

Ogni applicazione e ogni sistema operativo ha un modello di dati astratto. Molte applicazioni non espongono in modo esplicito questo modello di dati, ma il modello Guida il modo in cui viene scritto il codice dell'applicazione. Nel modello di programmazione a 32 bit (noto come modello ILP32), i tipi di dati Integer, Long e Pointer hanno una lunghezza di 32 bit. La maggior parte degli sviluppatori ha utilizzato questo modello senza rendersene conto. Per la cronologia dell'API Win32, si tratta di un presupposto valido (anche se non necessariamente sicuro) da eseguire.

In 64-bitWindows, questo presupposto di parità nelle dimensioni del tipo di dati non è valido. La lunghezza di tutti i tipi di dati 64 bit può comportare lo spreco di spazio, perché la maggior parte delle applicazioni non necessita delle dimensioni maggiori. Tuttavia, le applicazioni necessitano di puntatori a dati a 64 bit e hanno la possibilità di avere tipi di dati a 64 bit nei casi selezionati. Queste considerazioni hanno portato alla selezione di un modello di dati astratto denominato LLP64 (o P64). Nel modello di dati LLP64 solo i puntatori si espandono fino a 64 bit; tutti gli altri tipi di dati di base (Integer e Long) rimangono 32 bit di lunghezza.

Inizialmente, la maggior parte delle applicazioni eseguite in Windows a 64 bit sarà stata trasferita da Windows a 32 bit. Si tratta di un obiettivo che la stessa origine, scritta attentamente, deve essere eseguita su Windows a 32 e 64 bit. La definizione del modello di dati non semplifica questa attività. Tuttavia, verificare che il modello di dati influisca solo sui tipi di dati del puntatore è il primo passaggio. Il secondo passaggio consiste nel definire un set di nuovi tipi di dati che consentono agli sviluppatori di ridimensionare automaticamente i dati relativi al puntatore. Ciò consente ai dati associati ai puntatori di modificare le dimensioni, in quanto le dimensioni del puntatore cambiano da 32 bit a 64 bit. I tipi di dati di base rimangono 32 bit, pertanto non è possibile modificare le dimensioni dei dati sul disco, i dati condivisi in una rete o i dati condivisi tramite file mappati alla memoria. Questo consente agli sviluppatori di gran parte degli sforzi necessari per trasferire codice a 32 bit a Windows a 64 bit.

Questi nuovi tipi di dati sono stati aggiunti ai file di intestazione dell'API Windows. Pertanto, è possibile iniziare a utilizzare i nuovi tipi ora. Per ulteriori informazioni, vedere [i nuovi tipi di dati](the-new-data-types.md).

 

 




