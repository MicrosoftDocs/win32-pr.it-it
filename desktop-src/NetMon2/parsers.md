---
description: Un parser è il componente Network Monitor che controlla i dati in un'acquisizione ritardata e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser. Un parser è passivo perché funziona solo quando Network Monitor o un esperto lo chiama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878634"
---
# <a name="parser"></a>Parser

Un parser è il componente Network Monitor che controlla i dati in un' [*acquisizione ritardata*](d.md)e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser. Un parser è passivo perché funziona solo quando Network Monitor o un [*esperto*](e.md) lo chiama.

Ogni parser identifica un protocollo e in genere un parser viene implementato all'interno della propria DLL del parser. Una DLL del parser può tuttavia contenere più parser, il che significa che una DLL può essere usata per rilevare più di un protocollo.

I dati passati a un parser vengono ricavati da un' [*acquisizione ritardata*](d.md)e passati al parser in base ai frame. Non è possibile analizzare un'acquisizione in tempo reale.

Per analizzare i dati in un frame, il parser deve riconoscere l'istanza del protocollo, identificare le proprietà presenti nell'istanza del protocollo e alleghi una definizione di proprietà a ogni proprietà. Tenere presente che il frame contiene solo un flusso di dati. Il frame non contiene dati che indicano quali protocolli o proprietà del protocollo rappresentano i dati.

Nella figura seguente viene illustrato un frame contenente un'istanza di un protocollo.

![frame che contiene un'istanza di protocollo](images/parser1.png)

Se Network Monitor Visualizza i dati analizzati nell'interfaccia utente, il parser deve formattare i dati. Tuttavia, alcuni esperti usano l'output del parser a livello di codice e non visualizzano l'output nell'interfaccia utente di Network Monitor. I dati visualizzati includono i dati definiti dal parser e i dati nell'acquisizione. Il parser, ad esempio, in genere fornisce un nome per una proprietà visualizzata e i dati nell'acquisizione associata alla proprietà.



| Per informazioni su                                         | Vedere                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Quali punti di ingresso devono essere implementati all'interno della DLL del parser. | [Architettura DLL parser](parser-dll-architecture.md)                 |
| Come implementare le funzioni di esportazione della DLL del parser.                 | [Scrittura di un parser di protocollo](writing-a-protocol-parser.md)             |
| Funzioni e parser di strutture utilizzati da.                   | [Funzioni e strutture del parser](parser-functions-and-structures.md) |



 

 

 



