---
description: Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle strutture TAPI, ad eccezione di TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Strutture TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311850"
---
# <a name="tspi-structures"></a>Strutture TSPI

Le strutture di dati utilizzate da TSPI sono identiche a quelle definite nelle [strutture TAPI](./tapi-structures.md), ad eccezione di [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

Nel caso della maggior parte delle strutture di dati più grandi, la responsabilità di compilare i membri è divisa tra il provider di servizi e TAPI. Il provider di servizi deve mantenere i valori presenti nei membri di proprietà di TAPI. La descrizione dei membri che devono essere impostati dal provider di servizi e che devono essere conservati viene fornita nella sezione funzioni delle funzioni che fanno riferimento a tale struttura di dati.

Per ogni struttura, nella sezione Reference sono elencati gli elementi seguenti:

-   Scopo della struttura
-   Descrizione dei valori o dei campi
-   Descrizione dell'estendibilità della struttura
-   Commenti facoltativi sull'utilizzo della struttura
-   Riferimenti facoltativi ad altre funzioni, messaggi, costanti o strutture.

Memoria per tutte le strutture di dati la cui rappresentazione è pubblicata e condivisa da TAPI e il provider di servizi viene allocato da TAPI o da un'applicazione che usa TAPI. TAPI passa un puntatore alla funzione TSPI che restituisce le informazioni. TSPI riempie la struttura dei dati con le informazioni richieste. Se l'operazione è asincrona, le informazioni non sono disponibili fino a quando il callback di risposta asincrona non indica l'esito positivo.

> [!Note]  
> Alcune strutture includono campi di ridimensionamento e offset per la definizione della posizione e della lunghezza delle stringhe nella parte variabile della struttura. Se al provider di servizi viene richiesto di aggiungere una stringa ma non è disponibile alcuna stringa, il provider di servizi deve indicare questa condizione in uno dei modi seguenti:
>
> -   Impostare i campi dimensioni e offset su 0.
> -   Impostare il campo Offset su un valore diverso da zero, ma ridimensionarlo su 0.
> -   Impostare il campo Offset su un valore diverso da zero, dimensioni su 1 e byte in corrispondenza dell'offset su 0.

 

 

 
