---
description: I riconoscitori Microsoft usano i GUID seguenti.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4883ee713122ae36c4ad7e29b86013beb670545ffac31da28bad4da8c2f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031659"
---
# <a name="property-guids"></a>GUID di proprietà

I riconoscitori Microsoft usano i GUID seguenti. Quando possibile, le applicazioni devono usare questi GUID. Tuttavia, è previsto e consigliato che altri riconoscitori usino GUID aggiuntivi per le proprietà non supportate dai riconoscitori Microsoft.

Tutte le funzioni di proprietà sono state sviluppate con la comprensione che l'elenco di GUID può essere esteso da altri riconoscitori. Queste funzioni di proprietà includono:

-   [**Funzione GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**Funzione GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**Funzione GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**Funzione SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

La tabella seguente elenca i GUID delle proprietà di Tablet PC definiti in msinkaut.h (installato in c: Programmi \\ Microsoft Tablet PC Platform SDK Include per impostazione \\ \\ predefinita).



| GUID                                                  | Definizione                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Indice della casella alternativa del riconoscitore in modalità casella<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | Numero di riga<br/>                                                                   |
| SEGMENTAZIONE DI INKRECOGNITIONPROPERTY \_<br/>       | Segmentazione di parole e caratteri da parte del riconoscitore<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | Punto ad accesso rapido del movimento<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Numero massimo di tratti per un segmento<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | Metrica punti per pollice<br/>                                                        |
| CONFIDENCELEVEL DI INKRECOGNITIONPROPERTY \_<br/>    | [**CONFIDENZA \_ Enumerazione LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level)<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Informazioni per il calcolo della linea di base, della linea mediana o di entrambe, usate nel reticolo<br/> |



 

 

 




