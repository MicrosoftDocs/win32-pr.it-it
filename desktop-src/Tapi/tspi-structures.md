---
description: Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle strutture TAPI, ad eccezione di TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Strutture TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c11700dcaa46284b4050908ca70ed640e03afeb2eb7a2269ad1bac9161c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139754"
---
# <a name="tspi-structures"></a>Strutture TSPI

Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle strutture [TAPI,](./tapi-structures.md)ad eccezione di [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

Nel caso della maggior parte delle strutture di dati più grandi, la responsabilità di compilare i membri è suddivisa tra il provider di servizi e TAPI. Il provider di servizi deve mantenere i valori presenti nei membri di proprietà di TAPI. La descrizione dei membri che devono essere impostati dal provider di servizi e che devono essere mantenuti è disponibile nella sezione Funzioni delle funzioni che fanno riferimento a tale struttura di dati.

Per ogni struttura, la sezione di riferimento elenca gli elementi seguenti:

-   Scopo della struttura
-   Descrizione dei valori o dei campi
-   Descrizione dell'estendibilità della struttura
-   Commenti facoltativi sull'uso della struttura
-   Riferimenti facoltativi ad altre funzioni, messaggi, costanti o strutture.

La memoria per tutte le strutture di dati la cui rappresentazione viene pubblicata e condivisa sia da TAPI che dal provider di servizi viene allocata da TAPI o da un'applicazione tramite TAPI. TAPI passa un puntatore alla funzione TSPI che restituisce le informazioni. TSPI riempie la struttura dei dati con le informazioni richieste. Se l'operazione è asincrona, le informazioni non sono disponibili finché il callback di risposta asincrono non indica l'esito positivo.

> [!Note]  
> Alcune strutture includono i campi Size e Offset per definire la posizione e la lunghezza delle stringhe nella parte variabile della struttura. Se al provider di servizi viene richiesto di aggiungere una stringa ma non è disponibile alcuna stringa, il provider di servizi deve indicare questa condizione in uno dei modi seguenti:
>
> -   Impostare entrambi i campi Dimensioni e Offset su 0.
> -   Impostare il campo Offset su un valore diverso da zero, ma Size su 0.
> -   Impostare il campo Offset su un valore diverso da zero, Size su 1 e il byte in offset su 0.

 

 

 
