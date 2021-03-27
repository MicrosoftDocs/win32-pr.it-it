---
description: Le applicazioni che usano la metrica testo TrueType possono ottenere un elevato livello di portabilità della stampante e dei documenti; possono usare le metriche TrueType anche se devono mantenere la compatibilità con le prime versioni a 16 bit di Windows.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Uso della metrica TrueType portatile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994565"
---
# <a name="using-portable-truetype-metrics"></a>Uso della metrica TrueType portatile

Le applicazioni che usano la metrica testo TrueType possono ottenere un elevato livello di portabilità della stampante e dei documenti; possono usare le metriche TrueType anche se devono mantenere la compatibilità con le prime versioni a 16 bit di Windows.

Le larghezze di progettazione superano la maggior parte dei problemi del testo dipendente dal dispositivo introdotto dai dispositivi fisici. Le larghezze di progettazione sono un tipo di larghezza logica. Indipendentemente da eventuali problemi di rasterizzazione o da trasformazioni di ridimensionamento, ogni glifo ha una larghezza e un'altezza logiche. Composto da una pagina logica, ogni carattere in una stringa ha una posizione indipendente dalle larghezze del dispositivo fisico. Sebbene una larghezza logica implichi che le larghezze possano essere ridimensionate in modo lineare a tutti i punti, questa situazione non è necessariamente valida per i tipi di carattere non portabili o per la maggior parte dei tipi TrueType. Con le dimensioni dei punti più piccoli, alcuni glifi vengono resi più ampi rispetto alla relativa altezza per una migliore leggibilità.

I caratteri dei tipi di carattere TrueType Core sono progettati in base a una griglia 2048 di 2048. La larghezza di progettazione è la larghezza di un carattere in queste unità di griglia. (TrueType supporta qualsiasi dimensione della griglia Integer fino a 16.384 per 16.384; le dimensioni della griglia che sono potenze Integer di 2 scala più velocemente rispetto ad altre dimensioni della griglia).

Il contorno dei tipi di carattere è progettato in unità fittizie. Il quadrato em è la griglia teorica sulla quale viene inserito il contorno dei tipi di carattere. È possibile usare il membro **otmEMSquare** di [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) e il membro **ntmSizeEM** di [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) per recuperare le dimensioni del quadrato em nelle unità nozioni. Quando viene creato un tipo di carattere che ha una dimensione in punti (in unità dispositivo) uguale alla dimensione del quadrato em, le larghezze ABC per questo tipo di carattere sono le larghezze di progettazione desiderate. Si supponga, ad esempio, che le dimensioni di un quadrato em siano pari a 1000, mentre le larghezze ABC di un carattere nel tipo di carattere siano 150, 400 e 150. Un carattere in questo tipo di carattere che corrisponde a 10 unità di dispositivo alta avrà larghezze ABC rispettivamente di 1,5, 4 e 1,5. Poiché la \_ modalità di mapping del testo mm è più comunemente utilizzata con i tipi di carattere (e il \_ testo mm equivale a unità dispositivo), si tratta di un calcolo semplice.

A causa dell'elevata risoluzione delle larghezze di progettazione TrueType, le applicazioni che le utilizzano devono tener conto dei valori numerici di grandi dimensioni che è possibile creare. Per altre informazioni, vedere i seguenti argomenti:

-   [Dispositivo e unità di progettazione](device-vs--design-units.md)
-   [Metriche per documenti portatili](metrics-for-portable-documents.md)

 

 



