---
description: I codici di errore seguenti sono specifici dell'API di installazione.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Codici di errore (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485533"
---
# <a name="error-codes-setup-api"></a>Codici di errore (API di installazione)

I codici di errore seguenti sono specifici dell'API di installazione.



| Errori di analisi INF              | Descrizione                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ previsto \_ nome della sezione \_  | Il nome di una sezione è previsto e non è stato trovato.                                                                          |
| \_ \_ \_ riga nome sezione non valida errore \_ | Il formato del nome della sezione non è corretto. (Ad esempio, un nome non terminato da una parentesi graffa destra ( \] ). |
| nome della sezione di errore \_ \_ \_ troppo \_ lungo | Il nome della sezione supera la lunghezza massima del nome della sezione MAX \_ \_ \_ Len.                                               |
| \_sintassi generale \_ errore          | La sintassi generale non è corretta.                                                                                    |



 



| Errori di runtime INF         | Descrizione                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ di \_ tipo inf errato \_   | Il file INF non è del tipo specificato nella chiamata di funzione. Ad esempio, questo errore può essere restituito dalla funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) se il file inf è destinato a una versione precedente di Windows. |
| \_sezione errore \_ non \_ trovata | La sezione non è stata trovata nel file INF.                                                                                                                                                                                                     |
| riga di errore \_ \_ non \_ trovata    | La riga non è stata trovata nella sezione INF.                                                                                                                                                                                                     |



 

 

 



