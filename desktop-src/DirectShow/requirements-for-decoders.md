---
description: Requisiti per i decodificatori
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisiti per i decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481452"
---
# <a name="requirements-for-decoders"></a>Requisiti per i decodificatori

I decodificatori che inviano campioni a VMR devono rispettare le regole seguenti:

-   Deve essere recapitato un frame di sottoimmagine al VMR per ogni fotogramma video. I due frame dovrebbero avere gli stessi timestamp.
-   Se l'immagine non è stata modificata, usare il \_ flag AM GBF \_ NOTASYNCPOINT nel metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) per forzare l'allocatore a restituire un buffer contenente l'ultimo frame recapitato a VMR. È sufficiente inserire un nuovo timestamp sull'esempio e recapitarlo a VMR. Se la notorietà dell'immagine non è vuota, è necessario recapitarla. Il VMR rileverà il frame vuoto e non lo mescolerà con il video. Questo test viene eseguito dal chip VGA e non influisce sulle prestazioni di riproduzione.
-   Tutti gli esempi, ad eccezione dei flussi live, devono avere un timestamp di inizio e di fine valido collegati. Il DVD non è un flusso live.
-   I timestamp del campione multimediale devono essere contigui
-   Il decodificatore deve identificarsi come VMR per l'uso da parte di generatori di Graph.
-   Il flusso di sottoimmagine dovrebbe ora contenere valori alfa incorporati per pixel. Il tipo di superficie ARGB4444 è ideale per le immagini secondarie.
-   Non presupporre che lo stride della sottoimmagine sia uguale alla larghezza della superficie. Questo non è sempre il caso con VMR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'accelerazione video DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



