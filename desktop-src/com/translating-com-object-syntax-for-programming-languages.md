---
title: Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione
description: Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855998"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Traduzione della sintassi degli oggetti COM per i linguaggi di programmazione

Per chiamare un oggetto COM da un'applicazione scritta in un linguaggio di programmazione diverso da quello usato per scrivere l'oggetto COM, è necessario innanzitutto tradurre la sintassi dell'oggetto nel linguaggio di programmazione. Per effettuare questa operazione, utilizzare la procedura seguente:

1.  Visualizzare la libreria dei tipi dell'oggetto COM nella sintassi del linguaggio di programmazione. In questo modo vengono fornite le descrizioni delle classi, delle interfacce, dei metodi, delle proprietà e degli eventi dell'oggetto nella sintassi del linguaggio in uso.

    I prodotti Microsoft Developer forniscono diversi strumenti per semplificare la visualizzazione e la conversione delle librerie dei tipi. Per altre informazioni, vedere [visualizzatori e strumenti di conversione della libreria dei tipi](type-library-viewers-and-conversion-tools.md) e [come strumenti di sviluppo usare le librerie dei tipi](how-developer-tools-use-type-libraries.md).

    Quando è possibile visualizzare la libreria dei tipi dell'oggetto nel linguaggio di programmazione preferito, è possibile confrontare la relativa sintassi con quella nella documentazione relativa all'oggetto. Se l'oggetto è documentato in un linguaggio di programmazione diverso da quello in uso, i tipi di dati e la sintassi potrebbero essere diversi, ma le descrizioni dei parametri, i valori restituiti e la funzionalità dell'oggetto devono essere uguali.

2.  Prendere in considerazione eventuali considerazioni speciali per la conversione nel linguaggio di programmazione.

    Poiché ogni linguaggio di programmazione definisce concetti che non possono avere un equivalente in altre lingue, alcune funzionalità di un oggetto possono funzionare in modo diverso in un altro linguaggio o non essere disponibili. Il linguaggio di programmazione Visual Basic, ad esempio, non riconosce i tipi di dati non firmati C++, ad esempio **unsignedÂ Long**. Un'applicazione scritta in Visual Basic non può utilizzare metodi COM che accettano o restituiscono variabili con tipo di dati senza segno.

3.  Aggiungere il codice compilato dell'oggetto COM al progetto. Il codice compilato è in genere contenuto in un file con estensione dll o ocx. Questo passaggio è necessario affinché il compilatore riconosca le classi dell'oggetto COM. Dopo aver aggiunto l'oggetto COM, l'applicazione può utilizzare le classi e le interfacce.

Negli argomenti seguenti viene descritto come tradurre e utilizzare oggetti COM in un'ampia gamma di linguaggi di programmazione:

-   [Conversione in C++](translating-to-c--.md)
-   [Conversione in Visual Basic](translating-to-visual-basic.md)
-   [Conversione in Java](translating-to-java.md)

Questi argomenti descrivono gli strumenti e i processi di conversione forniti dai prodotti Microsoft Developer. Per istruzioni su come programmare gli oggetti COM usando gli strumenti di sviluppo creati da altre società, vedere la documentazione relativa agli strumenti di sviluppo.

 

 




