---
title: Modelli di dati astratti
description: Ogni applicazione e ogni sistema operativo ha un modello di dati astratto.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- modelli di dati astratti a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ad383e52c49997e43aa90301e7e417ef8cfeb089c9f6da151542b193b25071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121861"
---
# <a name="abstract-data-models"></a>Modelli di dati astratti

Ogni applicazione e ogni sistema operativo ha un modello di dati astratto. Molte applicazioni non espongono in modo esplicito questo modello di dati, ma il modello guida il modo in cui viene scritto il codice dell'applicazione. Nel modello di programmazione a 32 bit (noto come modello ILP32), i tipi di dati integer, long e puntatore hanno una lunghezza di 32 bit. La maggior parte degli sviluppatori ha usato questo modello senza rendersene conto. Per la cronologia dell'API Win32, si tratta di un presupposto valido (anche se non necessariamente sicuro).

In Windows a 64 bit questo presupposto di parità nelle dimensioni del tipo di dati non è valido. Rendere tutti i tipi di dati di lunghezza pari a 64 bit sprecherebbe spazio, perché la maggior parte delle applicazioni non ha bisogno di dimensioni maggiori. Tuttavia, le applicazioni necessitano di puntatori a dati a 64 bit e hanno la possibilità di avere tipi di dati a 64 bit in casi selezionati. Queste considerazioni hanno portato alla selezione di un modello di dati astratto denominato LLP64 (o P64). Nel modello di dati LLP64, solo i puntatori si espandono a 64 bit; tutti gli altri tipi di dati di base (integer e long) hanno una lunghezza di 32 bit.

Inizialmente, la maggior parte delle applicazioni che vengono eseguite in Windows a 64 bit sarà stata con ported da un Windows a 32 bit. Si tratta di un obiettivo che la stessa origine, scritta con attenzione, deve essere eseguita sia in versione a 32 che a 64 bit Windows. La definizione del modello di dati non semplifica questa attività. Tuttavia, assicurarsi che il modello di dati influisca solo sui tipi di dati puntatore è il primo passaggio. Il secondo passaggio consiste nel definire un set di nuovi tipi di dati che consentono agli sviluppatori di ridimensionare automaticamente i dati correlati al puntatore. Ciò consente ai dati associati ai puntatori di modificare le dimensioni quando le dimensioni del puntatore cambiano da 32 bit a 64 bit. I tipi di dati di base hanno una lunghezza di 32 bit, quindi le dimensioni dei dati sul disco, i dati condivisi in rete o i dati condivisi tramite file mappati alla memoria non cambiano. Ciò consente agli sviluppatori di eseguire gran parte del lavoro necessario per convertire il codice a 32 bit in codice a 64 bit Windows.

Questi nuovi tipi di dati sono stati aggiunti ai Windows di intestazione dell'API. È quindi possibile iniziare a usare i nuovi tipi ora. Per altre informazioni, vedere [Nuovi tipi di dati](the-new-data-types.md).

 

 




