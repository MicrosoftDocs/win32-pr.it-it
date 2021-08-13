---
description: Gli oggetti WMContainer forniscono un controllo di basso livello sull'analisi e la scrittura di un file ASF (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componenti ASF WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4d39edd9241a856d5ef854d91bc1198cb090ddf653960b19905407c28279a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736744"
---
# <a name="wmcontainer-asf-components"></a>Componenti ASF WMContainer

Gli oggetti WMContainer forniscono un controllo di basso livello sull'analisi e la scrittura di un file ASF (Advanced Systems Format).

I [componenti ASF del livello](pipeline-layer-asf-components.md) pipeline usano internamente gli oggetti WMContainer. La maggior parte delle applicazioni deve usare i componenti della pipeline, anziché gli oggetti WMContainer. Usare WMContainer solo se è necessario un controllo di basso livello sull'analisi e la scrittura di un file ASF.

Il livello WMContainer include gli oggetti seguenti:

-   [Profilo ASF](asf-profile.md)
-   [Oggetto ContentInfo di ASF](asf-contentinfo-object.md)
-   [Barra di divisione ASF](asf-splitter.md)
-   [ASF Multiplexer](asf-multiplexer.md)
-   [Indicizzatore ASF](asf-index-object.md)

Gli argomenti seguenti contengono istruzioni dettagliate sull'uso di WMContainer per leggere o scrivere file ASF.

-   [Esercitazione: Lettura di un file ASF tramite oggetti WMContainer](tutorial--reading-an-asf-file.md)
-   [Esercitazione: Copia di Flussi ASF tramite oggetti WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Esercitazione: Scrittura di un file WMA tramite oggetti WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Informazioni sul contenitore WM

Gli oggetti WMContainer interagiscono direttamente con gli oggetti file ASF. Il diagramma seguente illustra la struttura del file ASF e gli oggetti WMContainer corrispondenti.

![diagramma che mostra la struttura del file asf e gli oggetti media foundation corrispondenti](images/asf-components01.png)

Ad eccezione della barra di divisione e del multiplexer, ognuno di questi oggetti supporta sia l'analisi (lettura) che la scrittura di file ASF. La barra di divisione viene usata solo per la lettura dei file ASF. Il multiplexer viene usato solo per la creazione di nuovi file ASF.

Tutte le operazioni eseguite dagli oggetti WMContainer sono sincrone, ovvero bloccano il thread chiamante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



