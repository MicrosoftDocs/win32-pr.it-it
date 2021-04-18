---
description: Elaborazione dei dati
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Elaborazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304090"
---
# <a name="processing-data"></a>Elaborazione dei dati

**Analisi dei dati multimediali**

Se il filtro analizza i dati multimediali, non considerare attendibili le intestazioni o altri dati autodescrittivi nel contenuto. Ad esempio, non considerare attendibili i valori delle dimensioni che vengono visualizzati nei blocchi AVI o nei pacchetti MPEG. Esempi comuni di questo tipo di errore includono:

-   Lettura di *n* byte di dati, in cui il valore di *n* deriva dal contenuto, senza controllare *n* rispetto alle dimensioni effettive del buffer.
-   Passaggio a un offset di byte all'interno di un buffer, senza verificare che l'offset rientri nel buffer.

Un'altra classe comune di errori implica la mancata convalida delle descrizioni del formato trovate nel contenuto. Ad esempio:

-   Una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) può essere seguita da una tabella dei colori. La struttura **BITMAPINFO** viene definita come una struttura **BITMAPINFOHEADER** seguita da una matrice di valori **RGBQUAD** che compongono la tabella dei colori. Le dimensioni della matrice sono determinate dal valore di **biClrUsed**. Non copiare mai una tabella dei colori in un **BITMAPINFO** senza prima controllare la dimensione del buffer allocato per la struttura **BITMAPINFO** .
-   Una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) potrebbe avere informazioni aggiuntive sul formato aggiunte alla struttura. Il membro **cbSize** specifica la dimensione delle informazioni aggiuntive.

Durante la connessione al pin, un filtro deve verificare che tutte le strutture di formato siano ben formate e contengano valori ragionevoli. In caso contrario, rifiutare la connessione. Nel codice che convalida la struttura del formato, prestare particolare attenzione all'overflow aritmetico. Ad esempio, in un **BITMAPINFOHEADER**, la larghezza e l'altezza sono valori **Long** a 32 bit, ma le dimensioni dell'immagine (che è una funzione del prodotto dei due) sono solo un valore **DWORD** .

Se i dati di formattazione dell'origine sono maggiori del buffer allocato, non troncare i dati di origine per poterli copiare nel buffer. In questo modo è possibile creare una struttura la cui dimensione implicita è maggiore delle dimensioni effettive. Ad esempio, un'intestazione bitmap potrebbe specificare una tabella della tavolozza che non esiste più. In alternativa, riallocare il buffer o semplicemente interrompere la connessione.

**Errori durante il flusso**

Quando il grafico è in esecuzione, se il filtro riceve contenuto non valido, deve terminare il flusso. Eseguire le operazioni seguenti:

-   Restituisce un codice di errore dalla **ricezione**.
-   Chiamare [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul filtro downstream.
-   Chiamare [**CBaseFilter:: NotifyEvent**](cbasefilter-notifyevent.md) per pubblicare un evento [**EC \_ ERRORABORT**](ec-errorabort.md) .

**Modifiche al formato**

Esistono diversi meccanismi per i filtri per modificare i formati a metà flusso. Ognuno di essi prevede più di un passaggio, che consente di creare le potenziali accettazioni false. Se il filtro riceve una richiesta di modifica del formato dinamico, deve rifiutare la richiesta oppure rispettare il nuovo formato al suo arrivo. Analogamente, non cambiare mai i formati, a meno che l'altro filtro non accetti. Per altre informazioni, vedere [Dynamic Format Changes](dynamic-format-changes.md).

 

 
