---
description: I codici di errore seguenti sono specifici dell'API di installazione.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Codici di errore (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c3955bd64f38946a59589259fc750892cfa9e84b3ef6e32ba2d9a5f6ca2244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887340"
---
# <a name="error-codes-setup-api"></a>Codici di errore (API di installazione)

I codici di errore seguenti sono specifici dell'API di installazione.



| Errori di analisi INF              | Descrizione                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ PREVISTO NOME DI \_ \_ SEZIONE  | È previsto un nome di sezione e non è stato trovato.                                                                          |
| ERRORE \_ NELLA RIGA DEL NOME DI SEZIONE NON \_ \_ \_ VALIDO | Il nome della sezione non è nel formato corretto. Ad esempio, un nome non terminato da una parentesi quadra chiusa ( \] ). |
| NOME \_ DELLA SEZIONE DI ERRORE TROPPO \_ \_ \_ LUNGO | Il nome della sezione ha superato la lunghezza massima di MAX \_ SECT \_ NAME \_ LEN.                                               |
| SINTASSI \_ GENERALE \_ DEGLI ERRORI          | La sintassi generale non è corretta.                                                                                    |



 



| Errori di runtime INF         | Descrizione                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ - STILE \_ INF \_ ERRATO   | Il file INF non è del tipo specificato nella chiamata di funzione. Ad esempio, questo errore può essere restituito dalla funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) se il file INF era destinato a una versione precedente di Windows. |
| SEZIONE \_ DEGLI ERRORI NON \_ \_ TROVATA | La sezione non è stata trovata nel file INF.                                                                                                                                                                                                     |
| RIGA \_ DI ERRORE NON \_ \_ TROVATA    | La riga non è stata trovata nella sezione INF.                                                                                                                                                                                                     |



 

 

 



