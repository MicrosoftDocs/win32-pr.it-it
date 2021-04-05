---
description: Gli oggetti WMContainer forniscono il controllo di basso livello sull'analisi e la scrittura di un file di formato Advanced Systems (ASF).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componenti ASF WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967637"
---
# <a name="wmcontainer-asf-components"></a>Componenti ASF WMContainer

Gli oggetti WMContainer forniscono il controllo di basso livello sull'analisi e la scrittura di un file di formato Advanced Systems (ASF).

I [componenti ASF del livello pipeline](pipeline-layer-asf-components.md) utilizzano internamente gli oggetti WMContainer. La maggior parte delle applicazioni deve usare i componenti della pipeline, anziché usare gli oggetti WMContainer. Utilizzare WMContainer solo se è necessario un controllo di basso livello sull'analisi e la scrittura di un file ASF.

Il livello WMContainer include gli oggetti seguenti:

-   [Profilo ASF](asf-profile.md)
-   [Oggetto ContentInfo ASF](asf-contentinfo-object.md)
-   [Barra di divisione ASF](asf-splitter.md)
-   [Multiplexer ASF](asf-multiplexer.md)
-   [Indicizzatore ASF](asf-index-object.md)

Negli argomenti seguenti sono contenute istruzioni dettagliate sull'utilizzo di WMContainer per la lettura o la scrittura di file ASF.

-   [Esercitazione: lettura di un file ASF usando oggetti WMContainer](tutorial--reading-an-asf-file.md)
-   [Esercitazione: copia di flussi ASF usando oggetti WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Esercitazione: scrittura di un file WMA usando oggetti WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Informazioni sul contenitore WM

Gli oggetti WMContainer interagiscono direttamente con gli oggetti file ASF. Il diagramma seguente mostra la struttura dei file ASF e gli oggetti WMContainer corrispondenti.

![diagramma che illustra la struttura dei file ASF e gli oggetti di Media Foundation corrispondenti](images/asf-components01.png)

Ad eccezione della barra di divisione e del multiplexer, ognuno di questi oggetti supporta sia l'analisi (lettura) che la scrittura dei file ASF. La barra di divisione viene utilizzata solo per la lettura dei file ASF. Multiplexer viene usato solo per la creazione di nuovi file ASF.

Tutte le operazioni eseguite dagli oggetti WMContainer sono sincrone, ovvero bloccano il thread chiamante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



