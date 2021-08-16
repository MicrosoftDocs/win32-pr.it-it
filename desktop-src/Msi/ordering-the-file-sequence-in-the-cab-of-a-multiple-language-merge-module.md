---
description: I moduli unione in più lingue, le trasformazioni del linguaggio e i file CAB devono essere creati in modo che l'ordine dei file corrisponda all'ordine specificato nella tabella File.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordinamento della sequenza di file nel file CAB di un modulo unione in più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942808"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>Ordinamento della sequenza di file nel file CAB di un modulo unione in più lingue

È necessario creare moduli unione in più lingue, trasformazioni di linguaggio e file CAB in modo che l'ordine dei file nel .cab corrisponda all'ordine di installazione dei file specificato nella tabella file [,](file-table.md)anche dopo l'applicazione della trasformazione del linguaggio. Se l'ordine nel modulo e nel .cab non corrisponde, non è possibile usare il modulo merge.

Assegnare a ogni file nel modulo un numero di sequenza univoco indipendente dalla lingua e quindi usare sempre tale numero di sequenza per il file. Usare la stessa sequenza quando si compila il file CAB e si crea una trasformazione del linguaggio.

Poiché il programma di installazione installa solo i file elencati nella tabella [file](file-table.md), l'uso di una sequenza di file globale nel file CAB, nella tabella [file](file-table.md)e nella trasformazione del linguaggio consente all'utilità di unione di ignorare eventuali file aggiuntivi archiviati nel file CAB non elencati nella tabella [file](file-table.md). È possibile che esistano altri file nel file CAB, ma non devono essere elencati nella [tabella file](file-table.md). Ad esempio, un modulo che installa Code.dll, English.dat, German.dat e French.dat può usare l'ordine di sequenza di file globale seguente.



| File        | Sequenza |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |
| German.Dat  | 3        |
| Francese.Dat  | 4        |



 

È quindi possibile creare trasformazioni linguistiche per modificare la tabella [file](file-table.md) del modulo per l'inglese, il tedesco o il francese.

[Tabella file](file-table.md) (parziale per l'inglese)



| File        | Sequenza |
|-------------|----------|
| Code.Dll    | 1        |
| English.Dat | 2        |



 

[Tabella file](file-table.md) (parziale per il tedesco)



| File       | Sequenza |
|------------|----------|
| Code.Dll   | 1        |
| German.Dat | 3        |



 

[Tabella file](file-table.md) (parziale per il francese)



| File       | Sequenza |
|------------|----------|
| Code.Dll   | 1        |
| Francese.Dat | 4        |



 

Per altre informazioni, vedere [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) e [Authoring Merge Module File Tables.](authoring-merge-module-file-tables.md)

 

 



