---
description: Network Monitor o la DLL del parser può formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formattazione dei dati visualizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525146"
---
# <a name="formatting-displayed-data"></a>Formattazione dei dati visualizzati

Network Monitor o la DLL del parser può formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.

Network Monitor fornisce un formattatore generico che fornisce i servizi di base necessari per visualizzare la maggior parte dei tipi di dati presenti all'interno di un protocollo. Tuttavia, il formattatore generico non supporta tutti i tipi di dati. Il formattatore generico, ad esempio, non supporta quanto segue:

-   Diversi tipi di indirizzi.
-   Nomi descrittivi di origine e di destinazione.
-   Identificatori di oggetto.
-   Tipi di dati integer di grandi dimensioni.
-   Tipi di dati a lunghezza variabile Small Integer.

Nell'esempio seguente vengono identificate due stringhe formattate per la proprietà ID dei privilegi.

-   La prima riga di codice mostra l'output del formattatore generico. L'output è basato sul tipo di dati.
-   La seconda riga di codice mostra l'output di un formattatore personalizzato con una stringa per i dati della proprietà.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Quando possibile, usare il formattatore generico per visualizzare i dati perché consente di controllare le dimensioni della DLL del parser e offre migliori funzionalità multipiattaforma per la DLL del parser.

 

 

 



