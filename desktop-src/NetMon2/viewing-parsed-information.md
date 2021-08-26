---
description: Il Network Monitor frame visualizza i dati analizzati in tre riquadri.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Visualizzazione delle informazioni analizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f01cfc0df45f2fb6ef0e1342d7fe54e5ed5701bad8ba1635dc13f4546b10e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962687"
---
# <a name="viewing-parsed-information"></a>Visualizzazione delle informazioni analizzate

Il Network Monitor frame visualizza i dati analizzati in tre riquadri. Nel riquadro superiore viene visualizzato un riepilogo del frame che include il protocollo identificato. Nel riquadro centrale vengono visualizzate le proprietà dei dati formattati che possono essere organizzate gerarchicamente come parte della visualizzazione del parser. Nel riquadro inferiore vengono visualizzati i dati non elaborati evidenziati selezionati nel riquadro centrale.

È possibile specificare la modalità di visualizzazione delle informazioni nel visualizzatore quando si sviluppa un parser personalizzato. Nella figura seguente viene illustrato come visualizzare le informazioni nel visualizzatore Network Monitor frame.

![Visualizzatore frame di network monitor](images/parseui.png)

> [!Note]  
> I parser non visualizzano frame. I parser riconoscono i campi nelle informazioni fornite e quindi inviano Network Monitor per visualizzare il frame. Il filtro è un'operazione di livello superiore che consente alle query di filtro di estendersi su più parser.

 

Nel parser usare solo funzioni che possono essere eseguite in applicazioni Microsoft Win32. Prima di collegare le proprietà ai dati non elaborati, un parser deve prima registrare tutte le proprietà possibili con il kernel Network Monitor dati. Il parser invia un messaggio al kernel per creare un database delle proprietà e quindi inserisce nel database delle proprietà tutte le proprietà possibili per il relativo protocollo. Ogni proprietà nel database delle proprietà contiene informazioni quali una descrizione testuale, un tipo di dati e un qualificatore utilizzati per formattare i dati non elaborati e una routine di formattazione utilizzata per visualizzare i dati.

 

 



