---
description: "Esistono diversi formati in cui è possibile archiviare i dati dell'input penna, tra cui:"
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formati dati input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088483400f6e4452f888793dd7b0ce78966050b65c35db9baf6e79c2f00061c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032309"
---
# <a name="ink-data-formats"></a>Formati dati input penna

Esistono diversi formati in cui è possibile archiviare i dati dell'input penna, tra cui:

-   Formato serializzato input penna (ISF)
-   HTML
-   Rich Text Format (RTF)
-   Formato binario
-   formati Extensible Markup Language (XML)

Formati diversi sono applicabili in circostanze diverse. Per interagire al meglio con gli Appunti, le applicazioni devono essere in grado di riconoscere e generare il maggior numero possibile di formati diversi.

Il formato più importante e di base che può essere usato per archiviare l'input penna è Ink Serialized Format (ISF). ISF fornisce una rappresentazione compatta ma completa di un singolo [**oggetto Ink.**](inkdisp-class.md)

Un formato altrettanto importante è HTML. I dati dell'input penna possono essere rappresentati in HTML in modo che possano essere visualizzati come immagine da applicazioni che non riconoscono l'input penna. Viene inoltre mantenuta la massima fedeltà dell'input penna. Per questi motivi e poiché si tratta di un formato comunemente compreso che consente la rappresentazione di molti tipi diversi di contenuto, Microsoft consiglia html come formato per la condivisione dell'input penna.

È anche possibile archiviare l'input penna in altri formati. Usando RTF come formato, è possibile incollare l'input penna nelle applicazioni che non riconoscono l'input penna, ad esempio Microsoft Word 2002. Questa operazione viene eseguita incorporando gli oggetti OLE che contengono input penna all'interno del formato RTF. È comunque possibile usare altri formati, ad esempio formati binari o basati su XML.

I formati che si sceglie per una determinata applicazione per copiare, incollare o serializzare l'input penna devono essere basati su risorse e esigenze specifiche delle applicazioni. Come minimo, un'applicazione deve essere in grado di copiare e incollare ISF, che consente il livello più basso di interoperabilità dell'input penna. Sia ISF che la possibilità di copiare e incollare ISF sono incorporati nella piattaforma Tablet PC. Tuttavia, molte applicazioni devono rappresentare contenuto più complesso, ad esempio una selezione contenente più oggetti input penna o testo formattato. In tal caso, un'applicazione può copiare e incollare codice HTML. Ciò consente una massima flessibilità. HTML è ampiamente comprensibile e facile da generare. Infine, anche le applicazioni che producono RTF o hanno una forte necessità di comunicare con le applicazioni meno recenti devono produrre un formato RTF.

> [!Note]  
> Nel corso della discussione sull'interoperabilità dell'input penna, bitmap, ISF e GIF sono formati di immagine. L'oggetto input penna di testo (tInk) e l'oggetto input penna dello sketch (sInk) sono oggetti OLE. Binary, HTML, XML e RTF sono formati di documento in cui vengono utilizzate le immagini.

 

La piattaforma Tablet PC fornisce API che consentono di generare e interpretare questi formati. Esistono molte opzioni che insieme devono soddisfare le esigenze di interoperabilità e persistenza di qualsiasi applicazione. Per altre informazioni sui formati input penna, vedere [Formati di persistenza](persistence-formats.md).

 

 



