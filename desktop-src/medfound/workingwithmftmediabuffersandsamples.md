---
description: Uso di buffer e esempi di supporti MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Uso di buffer e esempi di supporti MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351336"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Uso di buffer e esempi di supporti MFT

Il codec MFTs passa i dati multimediali avanti e indietro usando buffer e esempi di supporti.

Un buffer multimediale è un oggetto COM che gestisce un blocco di memoria, in genere per memorizzare i dati multimediali. Quando i dati vengono passati a o da un MFT, vengono sempre passati sotto forma di buffer multimediale.

Tutti i buffer multimediali espongono l'interfaccia **IMFMediaBuffer** . Questa interfaccia è progettata per qualsiasi tipo di dati. I buffer contenenti dati video spesso espongono anche **IMF2DBuffer**.

Un buffer multimediale ha una dimensione massima, ovvero la quantità di memoria allocata per il buffer. Per trovare le dimensioni massime, chiamare **IMFMediaBuffer:: GetMaxLength**. In qualsiasi momento, un buffer multimediale dispone anche di una lunghezza corrente, ovvero la quantità di dati validi nel buffer, che va da zero byte fino alla dimensione massima. Per ottenere la lunghezza corrente, chiamare **IMFMediaBuffer:: GetCurrentLength**. Quando viene creato il buffer, la lunghezza corrente è zero. Se si scrivono dati nel buffer, chiamare **IMFMediaBuffer:: SetCurrentLength** per aggiornare la lunghezza corrente.

Per accedere alla memoria nel buffer, chiamare **IMFMediaBuffer:: Lock**. Questo metodo restituisce un puntatore all'inizio del blocco di memoria. Al termine dell'utilizzo del puntatore, chiamare **IMFMediaBuffer:: Unlock**. Il metodo **Lock** non è un meccanismo di sincronizzazione dei thread. non garantisce che altri thread non possano accedere al buffer. Il metodo **Lock** viene usato per garantire che la memoria a cui si accede rimarrà valida fino a quando non si chiama il metodo **Unlock** .

Un oggetto di esempio multimediale (nel contesto di Media Foundation SDK) è un oggetto che contiene un elenco ordinato di zero o più buffer. Gli esempi di supporti espongono l'interfaccia **IMFSample** .

Per creare un nuovo esempio, chiamare la funzione **MFCreateSample** . Inizialmente, l'elenco di buffer dell'esempio è vuoto. Per aggiungere un buffer alla fine dell'elenco, chiamare **IMFSample:: AddBuffer**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> <dt>

[Uso di codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



