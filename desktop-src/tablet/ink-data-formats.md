---
description: 'Sono disponibili diversi formati in cui è possibile archiviare i dati di input penna, tra cui:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formati di dati Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342821"
---
# <a name="ink-data-formats"></a>Formati di dati Ink

Sono disponibili diversi formati in cui è possibile archiviare i dati di input penna, tra cui:

-   Formato ISF (Ink Serialized Format)
-   HTML
-   Rich Text Format (RTF)
-   Formato binario
-   Formati basati su Extensible Markup Language (XML)

Formati diversi sono applicabili in circostanze diverse. Per interagire più correttamente con gli appunti, le applicazioni devono essere in grado di riconoscere e generare il maggior numero possibile di formati diversi.

Il formato più importante e di base che può essere usato per archiviare l'input penna è il formato ISF (Ink Serialized Format). ISF fornisce una rappresentazione compatta ma completa di un singolo oggetto [**input penna**](inkdisp-class.md) .

Un formato ugualmente importante è HTML. I dati Ink possono essere rappresentati in HTML in modo che possano essere visualizzati come immagini da applicazioni che non riconoscono l'input penna. Viene inoltre mantenuta la fedeltà completa dell'input penna. Per questi motivi, e poiché si tratta di un formato comunemente compreso che consente la rappresentazione di molti tipi diversi di contenuto, Microsoft consiglia HTML come formato per la condivisione di input penna.

È anche possibile archiviare l'input penna in altri formati. Utilizzando il formato RTF, è possibile incollare l'input penna in applicazioni che non riconoscono l'input penna, ad esempio Microsoft Word 2002. Questa operazione viene eseguita incorporando oggetti OLE che contengono input penna all'interno di RTF. È possibile utilizzare altri formati, ad esempio formati binari o basati su XML.

I formati scelti per una particolare applicazione per copiare, incollare o serializzare l'input penna devono essere basati su specifiche esigenze e risorse specifiche per le applicazioni. Come minimo, un'applicazione deve essere in grado di copiare e incollare ISF, che consente il livello più basso di interoperabilità dell'input penna. Sia ISF che la possibilità di copiare e incollare ISF sono incorporati nella piattaforma Tablet PC. Tuttavia, molte applicazioni devono rappresentare contenuto più complesso, ad esempio una selezione contenente più oggetti input penna o testo formattato. In tal caso, un'applicazione può copiare e incollare HTML. Questo consente una quantità massima di flessibilità. HTML è ampiamente comprensibile e facile da generare. Infine, le applicazioni che producono già RTF o hanno una forte necessità di comunicare con le applicazioni meno recenti dovrebbero produrre anche un formato RTF.

> [!Note]  
> Per tutta la discussione sull'interoperabilità dell'input penna, bitmap, ISF e GIF sono formati di immagine. L'oggetto input penna (tInk) e l'oggetto Ink sketch (sInk) sono oggetti OLE. Binary, HTML, XML e RTF sono formati di documento in cui vengono utilizzate le immagini.

 

La piattaforma Tablet PC fornisce le API che consentono di generare e interpretare questi formati. Sono disponibili molte opzioni che insieme dovrebbero soddisfare le esigenze di interoperabilità e persistenza di qualsiasi applicazione. Per ulteriori informazioni sui formati di input penna, vedere [formati di persistenza](persistence-formats.md).

 

 



