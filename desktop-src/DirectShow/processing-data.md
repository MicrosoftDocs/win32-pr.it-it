---
description: Elaborazione dei dati
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Elaborazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff417b3e37c3be43c42fd0cf8545bce6bfb00caa361d34d8044d690169f7c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748171"
---
# <a name="processing-data"></a>Elaborazione dei dati

**Analisi dei dati multimediali**

Se il filtro analizza i dati multimediali, non considerare attendibili le intestazioni o altri dati autodescrittori nel contenuto. Ad esempio, non considerare attendibili i valori delle dimensioni visualizzati in blocchi RIFF AVI o pacchetti MPEG. Esempi comuni di questo tipo di errore includono:

-   Lettura *di N* byte di dati, in cui il valore di *N* deriva dal contenuto, senza controllare *N* rispetto alle dimensioni effettive del buffer.
-   Passaggio a un offset di byte all'interno di un buffer, senza verificare che l'offset sia compreso nel buffer.

Un'altra classe comune di errori prevede la non convalida delle descrizioni di formato trovate nel contenuto. Esempio:

-   Una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) può essere seguita da una tabella dei colori. La **struttura BITMAPINFO** è definita come struttura **BITMAPINFOHEADER** seguita da una matrice di valori **RGBQUAD** che costituiscono la tabella dei colori. Le dimensioni della matrice sono determinate dal valore di **biClrUsed.** Non copiare mai una tabella dei colori **in bitmapINFO** senza prima controllare le dimensioni del buffer allocato per la **struttura BITMAPINFO.**
-   Una [**struttura WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) potrebbe avere informazioni aggiuntive sul formato aggiunte alla struttura. Il **membro cbSize** specifica le dimensioni delle informazioni aggiuntive.

Durante la connessione pin, un filtro deve verificare che tutte le strutture di formato siano ben formate e contengano valori ragionevoli. In caso contrario, rifiutare la connessione. Nel codice che convalida la struttura del formato, prestare particolare attenzione all'overflow aritmetico. In un oggetto **BITMAPINFOHEADER,** ad esempio, la larghezza e l'altezza sono valori lunghi a 32 **bit,** ma la dimensione dell'immagine (che è una funzione del prodotto dei due) è solo un **valore DWORD.**

Se i dati di formato dell'origine sono maggiori del buffer allocato, non troncare i dati di origine per copiare i dati nel buffer. In questo modo è possibile creare una struttura la cui dimensione implicita è maggiore delle dimensioni effettive. Ad esempio, un'intestazione bitmap potrebbe specificare una tabella tavolozza che non esiste più. In alternativa, riallocare il buffer o semplicemente non stabilire la connessione.

**Errori durante lo streaming**

Quando il grafico è in esecuzione, se il filtro riceve contenuto in formato non valido, deve terminare lo streaming. Eseguire le operazioni seguenti:

-   Restituisce un codice di errore da **Receive.**
-   Chiamare [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul filtro downstream.
-   Chiamare [**CBaseFilter::NotifyEvent per**](cbasefilter-notifyevent.md) pubblicare un [**evento EC \_ ERRORABORT.**](ec-errorabort.md)

**Modifiche al formato**

Esistono diversi meccanismi per i filtri per modificare i formati nel flusso intermedio. Ognuno di essi prevede più di un passaggio, che crea il rischio di false accettazioni. Se il filtro riceve una richiesta di modifica del formato dinamico, deve rifiutare la richiesta oppure rispettare il nuovo formato all'arrivo. Analogamente, non cambiare mai i formati a meno che l'altro filtro non accetti. Per altre informazioni, vedere [Modifiche al formato dinamico.](dynamic-format-changes.md)

 

 
