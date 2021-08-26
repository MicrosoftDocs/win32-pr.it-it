---
description: Impostazione delle proprietà nelle origini
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Impostazione delle proprietà nelle origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06908f4f15a6d1107ce15e71679c92ec8065725ed883a6561df5cd21af3e13c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965021"
---
# <a name="setting-properties-on-sources"></a>Impostazione delle proprietà nelle origini

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Quando si crea un nuovo oggetto di origine, sono necessarie alcune proprietà da impostare e altre che è possibile impostare facoltativamente. È necessario impostare le proprietà seguenti.

-   Ora di inizio e di arresto, rispetto al resto della sequenza temporale. Chiamare il [**metodo IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md) Non impostare tempi sovrapposti sugli oggetti di origine all'interno della stessa traccia o causerà un comportamento non definito.
-   File multimediale da usare come clip di origine. Chiamare [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md).
-   Tempi di avvio e arresto dei supporti, rispetto al file di origine originale. Chiamare il [**metodo IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Eccezione: se l'origine è un'immagine non ancorata, non specificare i tempi dei supporti. Per altre informazioni sui tempi dei supporti, vedere [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Un oggetto di origine eredita il tipo di supporto dal gruppo padre, quindi non è necessario specificare un tipo di supporto.

Le proprietà facoltative includono quanto segue:

-   Modalità stretch. La modalità stretch specifica il modo in cui Microsoft® DirectShow® Editing Services (DES) esegue il rendering di un'origine le cui dimensioni non corrispondono alle dimensioni di output. Per impostazione predefinita, DES estende un'immagine senza mantenere le proporzioni. In alternativa, DES può ritagliare un'immagine o creare una casella di lettere. Chiamare il [**metodo IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md) per specificare la modalità stretch.
-   Durata del file di origine. Se si imposta questa proprietà prima di impostare gli orari dei supporti, DES convalida l'ora di arresto dei supporti e tronca l'ora di arresto se supera la durata del file. Ciò consente di evitare errori di rendering in un secondo momento. È possibile ottenere la durata del file usando il rilevamento dei supporti, come descritto in [Uso di Media Detector](using-the-media-detector.md). Chiamare il [**metodo IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md) per specificare la durata del file.
-   Numero di flusso. Per impostazione predefinita, un oggetto di origine usa il primo flusso del file che corrisponde al tipo di supporto del gruppo padre. Se un file contiene due o più flussi dello stesso tipo di supporto, selezionare il flusso da usare chiamando [**IAMTimelineSrc::SetStreamNumber**](iamtimelinesrc-setstreamnumber.md). È possibile usare il rilevamento multimediale per trovare il numero di flussi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle origini](working-with-sources.md)
</dt> </dl>

 

 



