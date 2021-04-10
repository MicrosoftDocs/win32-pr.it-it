---
description: Comportamento demux Clock
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento demux Clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048999"
---
# <a name="demux-clock-behavior"></a>Comportamento demux Clock

In modalità push, il Demultiplexer MPEG-2 (demux) espone l'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) . Funge da origine live, quindi verrà scelto come clock di riferimento del grafico per impostazione predefinita. Per ulteriori informazioni, vedere [Live Sources](live-sources.md) .

-   Per i flussi di trasporto, il demux sincronizza l'orologio con il flusso di PCR che corrisponde al flusso audio o video più recentemente mappato dall'applicazione. Internamente, demux tiene traccia delle tabelle PAT e PMT. Quando l'applicazione esegue il mapping di un PID del flusso elementare a un pin di output, demux Cerca il flusso di PCR per tale PID e usa tale flusso di PCR. Attualmente non è possibile specificare direttamente il PID PCR per l'applicazione.
-   Per i flussi di programma, demux sincronizza l'orologio con il flusso SCR.

La sincronizzazione dell'orologio del filtro per il flusso PCR o SCR impedisce l'overflow o l'underflow dei dati, cosa che può verificarsi se il clock del grafico varia dal clock del flusso. Il demux converte anche i valori dei PTS di PES in orari di riferimento DirectShow e usa questi valori per contrassegnare il timestamp degli esempi di supporti. Gli indicatori di data e ora si applicano al limite del frame successivo. non vi è alcuna garanzia che il limite del frame verrà allineato all'inizio dell'esempio di supporto.

Il demux garantisce che i timestamp aumentino in modo progressivo. Ciò significa, ad esempio, che se un flusso di trasporto include un segmento, ad esempio un annuncio commerciale creato con un clock diverso da quello del programma principale, il demux modificherà i timestamp di presentazione per nascondere la discontinuità temporale dai filtri downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



