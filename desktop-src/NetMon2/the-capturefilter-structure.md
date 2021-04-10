---
description: In Network Monitor il filtro di acquisizione viene definito dalla struttura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Struttura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966763"
---
# <a name="the-capturefilter-structure"></a>Struttura CAPTUREFILTER

In Network Monitor il [filtro di acquisizione](capture-filters.md) viene definito dalla struttura [**capturefilter**](capturefilter.md) . L'assenza o la combinazione di flag, valori ed espressioni determina quali frame verranno passati o eliminati dal driver Network Monitor. Nella figura seguente sono illustrate le tre aree dell'analisi del filtro di acquisizione: ETYPE/SAP, Address e pattern match.

![tre aree dell'analisi del filtro di acquisizione](images/capfilter.png)

La tabella seguente elenca la funzione di ogni elemento filtro di acquisizione.



| Filter - elemento                                       | Azione                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ETYPE/SAP](writing-etypesap-filter-portion.md)     | Valuta le impostazioni di ETYPE/SAP. La combinazione di flag determina i tipi o i valori di impostazione inclusi o esclusi.                                                                                    |
| [Indirizzo](writing-addresstable-filter-portion.md)   | Valuta gli indirizzi di origine e di destinazione e le coppie di indirizzi. Diverse combinazioni di flag determinano quali valori singoli o combinazioni di coppie di indirizzi sono inclusi o esclusi.                   |
| [Corrispondenza criterio](writing-the-patternmatch-filter.md) | Definisce le corrispondenze di modelli complessi all'interno di un frame. I flag vengono forniti per diversi tipi e offset. È possibile combinare le corrispondenze dei modelli con le istruzioni operatore AND o OR logiche.                              |
| [Ritaglio](clipping-a-frame.md)                     | Consente di riagganciare i frame in un modo specificato da diversi valori di byte. È possibile utilizzare solo questo elemento per ritagliare tutti i frame o utilizzarlo con altri elementi di filtro di acquisizione. ad esempio, per trovare e quindi ritagliare un singolo frame. |
| [**Trigger**](trigger.md)                           | Questo elemento del filtro di acquisizione è obsoleto. I trigger non fanno più parte di un filtro di acquisizione. sono ora contenute nei propri tag BLOB, che vengono specificati separatamente.                                     |



 

Un frame viene valutato rispetto a tutte e tre le parti del filtro di acquisizione. Pertanto, un frame trasmesso correttamente deve superare ogni elemento. Tenere presente che il driver Network Monitor valuta l'assenza di uno dei tre elementi come **true**. Il driver, ad esempio, valuta l'assenza di una sezione ETYPE/SAP "tutti i frame con qualsiasi valore ETYPE/SAP sono validi".

 

 



