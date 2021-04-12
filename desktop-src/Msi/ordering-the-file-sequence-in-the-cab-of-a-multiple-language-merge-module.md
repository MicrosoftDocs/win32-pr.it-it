---
description: È necessario creare moduli di Unione a più lingue, trasformazioni di linguaggio e file CAB in modo tale che l'ordine dei file corrisponda all'ordine specificato nella tabella file.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordinamento della sequenza di file nel file CAB di un modulo di Unione a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234033"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Ordinamento della sequenza di file nel file CAB di un modulo di Unione a più lingue

È necessario creare moduli di Unione a più lingue, trasformazioni di linguaggio e file CAB in modo tale che l'ordine dei file nel file CAB corrisponda all'ordine di installazione dei file specificati nella [tabella dei file](file-table.md), anche dopo l'applicazione della trasformazione del linguaggio. Se l'ordine nel modulo e nel file CAB non corrispondono, non è possibile usare il modulo merge.

Assegnare a ogni file nel modulo, un numero di sequenza univoco indipendente dalla lingua e quindi usare sempre il numero di sequenza per il file. Utilizzare la stessa sequenza quando si compila il file CAB e si crea una trasformazione di linguaggio.

Poiché il programma di installazione installa solo i file elencati nella [tabella file](file-table.md), l'utilizzo di una sequenza di file globale nel file CAB, nella [tabella file](file-table.md)e nella trasformazione lingua consente allo strumento di merge di ignorare eventuali file aggiuntivi archiviati nel file CAB che non sono elencati nella [tabella file](file-table.md). Nel file CAB possono esistere altri file, ma non devono essere elencati nella [tabella file](file-table.md). Ad esempio, un modulo che installa Code.dll, English. dat, German. dat e French. dat può utilizzare l'ordine di sequenza dei file globale seguente.



| File        | Sequenza |
|-------------|----------|
| Code.Dll    | 1        |
| Inglese. dat | 2        |
| Tedesco. dat  | 3        |
| Francese. dat  | 4        |



 

Le trasformazioni della lingua possono quindi essere create per modificare la [tabella dei file](file-table.md) del modulo per la lingua inglese, tedesca o francese.

[Tabella file](file-table.md) (parziale per l'inglese)



| File        | Sequenza |
|-------------|----------|
| Code.Dll    | 1        |
| Inglese. dat | 2        |



 

[Tabella file](file-table.md) (parziale per il tedesco)



| File       | Sequenza |
|------------|----------|
| Code.Dll   | 1        |
| Tedesco. dat | 3        |



 

[Tabella file](file-table.md) (parziale per il francese)



| File       | Sequenza |
|------------|----------|
| Code.Dll   | 1        |
| Francese. dat | 4        |



 

Per ulteriori informazioni, vedere [creazione di una trasformazione di linguaggio per un modulo di merge a più lingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md) e [creazione di tabelle di file di moduli merge](authoring-merge-module-file-tables.md).

 

 



