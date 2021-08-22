---
description: In Network Monitor, il filtro di acquisizione è definito dalla struttura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Struttura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5c6d8d8f8baa3710b7dff4e33c98eb8791a65dc76931caa9068bbc1280f33e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339366"
---
# <a name="the-capturefilter-structure"></a>Struttura CAPTUREFILTER

In Network Monitor, il [filtro di](capture-filters.md) acquisizione è definito dalla struttura [**CAPTUREFILTER.**](capturefilter.md) L'assenza o la combinazione di flag, valori ed espressioni determina quali frame verranno passati o eliminati dal driver Network Monitor. La figura seguente mostra le tre aree dell'analisi del filtro di acquisizione: Etype/SAP, indirizzo e corrispondenza del modello.

![tre aree dell'analisi del filtro di acquisizione](images/capfilter.png)

Nella tabella seguente viene elencata la funzione di ogni elemento filtro capture.



| Filter - elemento                                       | Azione                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etype/SAP](writing-etypesap-filter-portion.md)     | Valuta le impostazioni Etype/SAP. La combinazione di flag determina quali tipi di impostazione o valori vengono inclusi o esclusi.                                                                                    |
| [Indirizzo](writing-addresstable-filter-portion.md)   | Valuta gli indirizzi di origine e di destinazione e le coppie di indirizzi. Diverse combinazioni di flag determinano quali singoli valori o combinazioni di coppie di indirizzi vengono inclusi o esclusi.                   |
| [Criteri di ricerca](writing-the-patternmatch-filter.md) | Definisce corrispondenze di criteri complessi all'interno di un frame. I flag vengono forniti per tipi e offset diversi. È possibile combinare corrispondenze di criteri con istruzioni dell'operatore AND logico o OR.                              |
| [Ritaglio](clipping-a-frame.md)                     | Ritaglia i fotogrammi nel modo specificato da diversi valori di byte. È possibile usare solo questo elemento per ritagliare tutti i fotogrammi o usarlo con altri elementi filtro di acquisizione. ad esempio per trovare e quindi ritagliare un singolo fotogramma. |
| [**Trigger**](trigger.md)                           | Questo elemento filtro di acquisizione è obsoleto. I trigger non fanno più parte di un filtro di acquisizione. sono ora contenuti nei propri tag BLOB, che vengono specificati separatamente.                                     |



 

Un frame viene valutato rispetto a tutte e tre le parti del filtro di acquisizione. Pertanto, un frame trasmesso correttamente deve passare ogni elemento. Tenere presente che il driver Network Monitor valuta l'assenza di uno dei tre elementi come **TRUE.** Ad esempio, il driver valuta l'assenza di una sezione Etype/SAP come "TUTTI i frame con il valore ANY Etype/SAP sono validi".

 

 



