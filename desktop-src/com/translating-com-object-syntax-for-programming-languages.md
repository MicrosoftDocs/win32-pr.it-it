---
title: Conversione della sintassi degli oggetti COM per i linguaggi di programmazione
description: Conversione della sintassi degli oggetti COM per i linguaggi di programmazione
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6871046a80537dd39b4c9b502d945e28e46e719e637c4e6a629179dd3c6454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500081"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Conversione della sintassi degli oggetti COM per i linguaggi di programmazione

Per chiamare un oggetto COM da un'applicazione scritta in un linguaggio di programmazione diverso da quello usato per scrivere l'oggetto COM, è innanzitutto necessario convertire la sintassi dell'oggetto nel linguaggio di programmazione. Per effettuare questa operazione, utilizzare la procedura seguente:

1.  Visualizzare la libreria dei tipi dell'oggetto COM nella sintassi del linguaggio di programmazione. In questo modo vengono fornite le descrizioni delle classi, delle interfacce, dei metodi, delle proprietà e degli eventi dell'oggetto nella sintassi del linguaggio in uso.

    I prodotti per sviluppatori Microsoft offrono diversi strumenti che consentono di visualizzare e convertire le librerie dei tipi. Per altre informazioni, vedere [Visualizzatori e strumenti di conversione](type-library-viewers-and-conversion-tools.md) delle librerie dei [tipi e Come Strumenti di sviluppo le librerie dei tipi.](how-developer-tools-use-type-libraries.md)

    Quando è possibile visualizzare la libreria dei tipi dell'oggetto nel linguaggio di programmazione preferito, è possibile confrontarne la sintassi con quella nella documentazione relativa all'oggetto. Se l'oggetto è documentato in un linguaggio di programmazione diverso da quello in uso, i tipi di dati e la sintassi possono essere diversi, ma le descrizioni dei parametri, i valori restituiti e la funzionalità dell'oggetto devono essere uguali.

2.  Prendere in considerazione eventuali considerazioni speciali per la conversione nel linguaggio di programmazione.

    Poiché ogni linguaggio di programmazione definisce concetti che potrebbero non avere un equivalente in altri linguaggi, alcune funzionalità di un oggetto possono funzionare in modo diverso in un altro linguaggio o non essere disponibili. Ad esempio, il Visual Basic di programmazione non riconosce i tipi di dati senza segno C++, ad esempio **unsignedÂ long.** Un'applicazione scritta in Visual Basic non può usare metodi COM che accettano o restituiscono variabili del tipo di dati senza segno.

3.  Aggiungere il codice compilato dell'oggetto COM al progetto. Il codice compilato è in genere contenuto in un file .dll o ocx. Questo passaggio è necessario perché il compilatore riconosca le classi dell'oggetto COM. Dopo aver aggiunto l'oggetto COM, l'applicazione può usare le relative classi e interfacce.

Gli argomenti seguenti descrivono come tradurre e usare oggetti COM in un'ampia gamma di linguaggi di programmazione:

-   [Conversione in C++](translating-to-c--.md)
-   [Traduzione in Visual Basic](translating-to-visual-basic.md)
-   [Traduzione in Java](translating-to-java.md)

Questi argomenti descrivono gli strumenti e i processi di conversione forniti dai prodotti per sviluppatori Microsoft. Per istruzioni su come programmare oggetti COM usando strumenti di sviluppo creati da altre società, vedere la documentazione di tali strumenti di sviluppo.

 

 




