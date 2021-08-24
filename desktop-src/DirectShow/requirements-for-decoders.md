---
description: Requisiti per i decodificatori
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisiti per i decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84d02926b4ce36cea9e4221589d52690edb8e256b2f0f4863fa19fff5dc033
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697031"
---
# <a name="requirements-for-decoders"></a>Requisiti per i decodificatori

I decodificatori che forniscono esempi al VMR devono osservare le regole seguenti:

-   Deve essere presente un fotogramma immagine secondaria recapitato alla macchina virtuale per ogni fotogramma video. I due fotogrammi devono avere gli stessi timestamp.
-   Se l'immagine secondaria non è stata modificata, usare il flag AM GBF NOTASYNCPOINT nel metodo \_ \_ [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) per forzare l'allocatore a restituire un buffer contenente l'ultimo frame recapitato alla macchina virtuale. È sufficiente inserire un nuovo timestamp nell'esempio e recapitarlo nuovamente alla macchina virtuale. Se l'immagine secondaria è vuota, è comunque necessario recapitarla. La macchina virtuale rileverà il fotogramma vuoto e non lo sfuma con il video. Questo test viene eseguito dal chip VGA e non influisce sulle prestazioni di riproduzione.
-   Tutti gli esempi, ad eccezione dei flussi live, devono avere timestamp di inizio e arresto validi associati. Il DVD non è un flusso live.
-   I timestamp di esempio dei supporti devono essere contigui
-   Il decodificatore deve identificarsi come idoneo per vmr per l'uso da parte dei generatori di grafi.
-   Il flusso di immagini secondarie deve ora contenere valori alfa per pixel incorporati. Il tipo di superficie ARGB4444 è ideale per le immagini secondarie.
-   Non presupporre che lo stride dell'immagine secondaria sia uguale alla larghezza della superficie. Questo non è sempre il caso della macchina virtuale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'accelerazione video DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



