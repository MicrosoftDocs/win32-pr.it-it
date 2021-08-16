---
description: Comportamento dell'orologio demux
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento dell'orologio demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ab1976bf123e971f6c3ec08e18c743352d37b73de95901a67abfee5d10a054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821186"
---
# <a name="demux-clock-behavior"></a>Comportamento dell'orologio demux

In modalità push, il demultiplexer MPEG-2 (demux) espone [**l'interfaccia IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) Funge da origine live, quindi verrà scelto come orologio di riferimento del grafo per impostazione predefinita. Per [altre informazioni, vedere Origini](live-sources.md) in tempo reale.

-   Per i flussi di trasporto, il demux sincronizza l'orologio con il flusso PCR corrispondente al flusso audio o video mappato più di recente dall'applicazione. Internamente, il demux tiene traccia delle tabelle PAT e PMT. Quando l'applicazione esegue il mapping di un PID di flusso elementare a un pin di output, il demux cerca il flusso PCR per tale PID e usa tale flusso PCR. Attualmente l'applicazione non può specificare direttamente il PID PCR.
-   Per i flussi di programma, il demux sincronizza il clock con il flusso SCR.

La sincronizzazione dell'orologio del filtro con il flusso PCR o SCR impedisce l'overflow o il underflow dei dati, che potrebbe verificarsi se l'orologio del grafico varia rispetto all'orologio del flusso. Il demux converte anche i valori PTS PES in DirectShow di riferimento e usa questi valori per impostare il timestamp dei campioni multimediali. I timestamp si applicano al limite fotogramma successivo. non esiste alcuna garanzia che il limite del frame sia allineato all'inizio dell'esempio multimediale.

Il demux garantisce che i timestamp aumentino in modo monotona. Ciò significa, ad esempio, che se un flusso di trasporto include un segmento, ad esempio uno spot creato con un orologio diverso da quello del programma principale, il demux regola i timestamp di presentazione per nascondere la discontinuità temporale dai filtri downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



