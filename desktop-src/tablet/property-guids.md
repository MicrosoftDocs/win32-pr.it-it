---
description: I riconoscitori Microsoft usano i seguenti GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132027"
---
# <a name="property-guids"></a>GUID proprietà

I riconoscitori Microsoft usano i seguenti GUID. Laddove possibile, le applicazioni devono usare questi GUID. Tuttavia, è previsto che gli altri riconoscitori usino GUID aggiuntivi per le proprietà non supportate dai sistemi di riconoscimento Microsoft.

Tutte le funzioni di proprietà sono state sviluppate con la consapevolezza che l'elenco dei GUID può essere esteso da altri riconoscitori. Queste funzioni di proprietà includono:

-   [**GetContextPropertyList (funzione)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetContextPropertyValue (funzione)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList (funzione)**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetContextPropertyValue (funzione)**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

La tabella seguente elenca i GUID delle proprietà di Tablet PC definiti in msinkaut. h (installati in c: \\ programmi \\ Microsoft Tablet PC Platform SDK \\ includono per impostazione predefinita).



| GUID                                                  | Definizione                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| \_BOXNUMBER INKRECOGNITIONPROPERTY<br/>          | Indice della casella alternativa del riconoscitore in modalità Box<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | Numero di riga<br/>                                                                   |
| \_segmentazione INKRECOGNITIONPROPERTY<br/>       | Segmenti di parole e caratteri per il riconoscimento<br/>                                  |
| \_Hotpoint INKRECOGNITIONPROPERTY<br/>           | Punto critico del movimento<br/>                                                             |
| \_MAXIMUMSTROKECOUNT INKRECOGNITIONPROPERTY<br/> | Numero massimo di tratti per un segmento<br/>                                           |
| \_POINTSPERINCH INKRECOGNITIONPROPERTY<br/>      | Metrica dei punti per pollice<br/>                                                        |
| \_CONFIDENCELEVEL INKRECOGNITIONPROPERTY<br/>    | [**Sicurezza \_ Enumerazione LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level)<br/>                         |
| \_LINEMETRICS INKRECOGNITIONPROPERTY<br/>        | Informazioni per il calcolo della baseline, della linea media o di entrambe le informazioni utilizzate nel reticolo<br/> |



 

 

 




