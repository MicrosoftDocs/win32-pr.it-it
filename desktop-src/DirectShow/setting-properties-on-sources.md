---
description: Impostazione delle proprietà nelle origini
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Impostazione delle proprietà nelle origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875901"
---
# <a name="setting-properties-on-sources"></a>Impostazione delle proprietà nelle origini

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Quando si crea un nuovo oggetto di origine, è necessario impostare alcune proprietà, mentre altre possono essere impostate facoltativamente. È necessario impostare le proprietà seguenti.

-   Orari di inizio e di fine, relativi al resto della sequenza temporale. Chiamare il metodo [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . Non impostare tempi sovrapposti negli oggetti di origine all'interno della stessa traccia o causare un comportamento non definito.
-   File multimediale da utilizzare come clip di origine. Chiamare [**IAMTimelineSrc:: Semedianame**](iamtimelinesrc-setmedianame.md).
-   L'ora di inizio e di fine del supporto rispetto al file di origine originale. Chiamare il metodo [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Eccezione: se l'origine è ancora un'immagine, non specificare i tempi dei supporti. Per altre informazioni sui tempi dei supporti, vedere [Time in DirectShow editing Services](time-in-directshow-editing-services.md).

Un oggetto di origine eredita il tipo di supporto dal gruppo padre, pertanto non è necessario specificare un tipo di supporto.

Le proprietà facoltative includono quanto segue:

-   Modalità di estensione. La modalità Stretch specifica il modo in cui Microsoft® DirectShow® editing Services (DES) esegue il rendering di un'origine la cui dimensione non corrisponde alle dimensioni di output. Per impostazione predefinita, DES estende un'immagine senza mantenere le proporzioni. In alternativa, le DES possono ritagliare un'immagine o creare una letterbox. Chiamare il metodo [**IAMTimelineSrc:: SetStretchMode**](iamtimelinesrc-setstretchmode.md) per specificare la modalità di estensione.
-   Durata del file di origine. Se si imposta questa proprietà prima di impostare i tempi dei supporti, DES convalida l'ora di arresto del supporto e tronca l'ora di arresto se supera la durata del file. Ciò consente di evitare errori di rendering in un secondo momento. È possibile ottenere la durata del file usando il rilevatore multimediale, come descritto in [uso del rilevatore multimediale](using-the-media-detector.md). Chiamare il metodo [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md) per specificare la durata del file.
-   Numero del flusso. Per impostazione predefinita, un oggetto di origine usa il primo flusso del file che corrisponde al tipo di supporto del gruppo padre. Se un file contiene due o più flussi dello stesso tipo di supporto, selezionare il flusso da utilizzare chiamando [**IAMTimelineSrc:: SetStreamNumber**](iamtimelinesrc-setstreamnumber.md). È possibile usare il rilevatore multimediale per trovare il numero di flussi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di origini](working-with-sources.md)
</dt> </dl>

 

 



