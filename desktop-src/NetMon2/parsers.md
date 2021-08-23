---
description: Un parser è il Network Monitor che controlla i dati in un'acquisizione ritardata e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser. Un parser è passivo perché funziona solo quando Network Monitor o un esperto lo chiama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf6f7c799782a75905d366c56157a99fd6f774f5682e302dcec4a9d6c788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555516"
---
# <a name="parser"></a>Parser

Un parser è il Network Monitor che controlla i [](d.md)dati in un'acquisizione ritardata e passa informazioni specifiche sul protocollo all'applicazione che chiama il parser. Un parser è passivo perché funziona solo quando Network Monitor o [*un esperto*](e.md) lo chiama.

Ogni parser identifica un protocollo e, in genere, un parser viene implementato all'interno della propria DLL del parser. Tuttavia, una DLL del parser può contenere più parser, il che significa che una DLL può essere usata per rilevare più di un protocollo.

I dati passati a un parser vengono prelevati da un'acquisizione ritardata e passati al parser frame per frame. [](d.md) Non è possibile analizzare un'acquisizione in tempo reale.

Per analizzare i dati in un frame, il parser deve riconoscere l'istanza del protocollo, identificare le proprietà esistenti nell'istanza del protocollo e associare una definizione di proprietà a ogni proprietà. Tenere presente che il frame contiene solo un flusso di dati. Il frame non contiene dati che indicano quali protocolli o proprietà del protocollo rappresentano i dati.

Nella figura seguente viene illustrato un frame che contiene un'istanza di un protocollo.

![frame che contiene un'istanza del protocollo](images/parser1.png)

Se Network Monitor visualizza i dati analizzati nell'interfaccia utente, il parser deve formattare i dati. Tuttavia, alcuni esperti usano l'output del parser a livello di codice e non visualizzano l'output nell'interfaccia Network Monitor interfaccia utente. I dati visualizzati includono sia i dati definiti dal parser che i dati nell'acquisizione. Ad esempio, il parser fornisce in genere sia un nome per una proprietà visualizzata che i dati nell'acquisizione associati alla proprietà.



| Per informazioni su                                         | Vedere                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Quali punti di ingresso devono essere implementati all'interno della DLL del parser. | [Architettura della DLL del parser](parser-dll-architecture.md)                 |
| Come implementare le funzioni di esportazione dll del parser.                 | [Scrittura di un parser di protocollo](writing-a-protocol-parser.md)             |
| Funzioni e strutture usate dal parser.                   | [Funzioni e strutture del parser](parser-functions-and-structures.md) |



 

 

 



