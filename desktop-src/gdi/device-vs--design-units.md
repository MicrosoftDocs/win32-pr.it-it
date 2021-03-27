---
description: Un'applicazione può recuperare le metriche dei tipi di carattere per un tipo di carattere fisico solo dopo che il tipo di carattere è stato selezionato in un contesto di dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo e unità di progettazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880305"
---
# <a name="device-vs-design-units"></a>Dispositivo e unità di progettazione

Un'applicazione può recuperare le metriche dei tipi di carattere per un tipo di carattere fisico solo dopo che il tipo di carattere è stato selezionato in un contesto di dispositivo. Quando si seleziona un tipo di carattere in un contesto di dispositivo, questo viene ridimensionato per il dispositivo. Le metriche dei tipi di carattere specifiche del dispositivo sono note come unità del dispositivo.

Le metriche portabili nei tipi di carattere sono note come unità di progettazione. Per applicare a un dispositivo specifico, le unità di progettazione devono essere convertite in unità di dispositivo. Usare la formula seguente per convertire le unità di progettazione in unità di dispositivo.

*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*pointsize*/72) \* *DeviceResolution*

Le variabili in questa formula hanno i significati seguenti.



| Variabile           | Descrizione                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DeviceUnits*      | Specifica la metrica del tipo di carattere *DesignUnits* convertita in unità dispositivo. Questo valore si trova nelle stesse unità del valore specificato per *DeviceResolution*.                          |
| *DesignUnits*      | Specifica la metrica del tipo di carattere da convertire in unità di dispositivo. Questo valore può essere qualsiasi metrica del tipo di carattere, inclusa la larghezza di un carattere o il valore crescente per un intero tipo di carattere. |
| *unitsPerEm*       | Specifica la dimensione del quadrato em per il tipo di carattere.                                                                                                                                 |
| *PointSize*        | Specifica la dimensione del tipo di carattere, in punti. (Un punto è uguale a 1/72 di pollice).                                                                                                 |
| *DeviceResolution* | Specifica il numero di unità di dispositivo (pixel) per pollice. I valori tipici possono essere 300 per una stampante laser o 96 per una schermata VGA.                                                |



 

Questa formula non può essere usata per convertire le unità del dispositivo in unità di progettazione. Le unità del dispositivo sono sempre arrotondate al pixel più vicino. L'errore di arrotondamento propagato può diventare molto elevato, soprattutto quando un'applicazione utilizza dimensioni dello schermo.

Per richiedere unità di progettazione, creare un tipo di carattere logico la cui altezza è specificata come *unitsPerEm*. Le applicazioni possono recuperare il valore per *unitsPerEm* chiamando la funzione [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) e controllando il membro **ntmSizeEM** della struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .

 

 



