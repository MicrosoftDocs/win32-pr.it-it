---
description: Il Visualizzatore frame Network Monitor Visualizza i dati analizzati in tre riquadri.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Visualizzazione di informazioni analizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568284"
---
# <a name="viewing-parsed-information"></a>Visualizzazione di informazioni analizzate

Il Visualizzatore frame Network Monitor Visualizza i dati analizzati in tre riquadri. Il riquadro superiore Visualizza un riepilogo del frame che include il protocollo identificato. Nel riquadro centrale vengono visualizzate le proprietà dei dati formattate che possono essere organizzate in modo gerarchico come parte della visualizzazione del parser. Nel riquadro inferiore vengono visualizzati i dati non elaborati evidenziati selezionati nel riquadro centrale.

È possibile specificare la modalità di visualizzazione delle informazioni nel visualizzatore quando si sviluppa un parser personalizzato. Nella figura seguente viene illustrato il modo in cui le informazioni possono essere visualizzate in Network Monitor Frame Viewer.

![Visualizzatore frame di Network Monitor](images/parseui.png)

> [!Note]  
> I parser non visualizzano i frame. I parser riconoscono i campi delle informazioni fornite, quindi notificano Network Monitor per visualizzare il frame. Il filtro è un'operazione di livello superiore che consente di filtrare le query per estendere i parser.

 

Nel parser usare solo le funzioni che possono essere eseguite in applicazioni Microsoft Win32. Prima di associare le proprietà ai dati non elaborati, un parser deve prima registrare tutte le possibili proprietà con il kernel Network Monitor. Il parser Invia un messaggio al kernel per creare un database di proprietà e quindi compila il database delle proprietà con tutte le possibili proprietà del protocollo. Ogni proprietà nel database delle proprietà contiene informazioni quali una descrizione testuale, un tipo di dati e un qualificatore utilizzati per formattare i dati non elaborati e una routine di formattazione utilizzata per visualizzare i dati.

 

 



