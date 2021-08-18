---
description: Esempio di filtri di origine push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Esempio di filtri di origine push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747791"
---
# <a name="push-source-filters-sample"></a>Esempio di filtri di origine push

## <a name="description"></a>Descrizione

Questo esempio è costituito da un set di tre filtri di origine che forniscono i dati di origine seguenti come flusso video:

-   CPushSourceBitmap: singola bitmap (caricata dalla directory corrente)
-   CPushSourceBitmapSet: set di bitmap (caricato dalla directory corrente)
-   CPushSourceDesktop: copia dell'immagine del desktop corrente (solo GDI)

## <a name="usage"></a>Utilizzo

Per usare un filtro, caricarlo in GraphEdit ed eseguirne il rendering del pin di output. In questo modo si connetterà un renderer video (ed eventualmente un filtro color space Converter) e sarà possibile visualizzare l'output. Se si vuole eseguire il rendering dell'output in un file AVI, caricare il mux AVI, caricare un filtro writer di file, fornire un nome di output al writer di file ed eseguire il rendering del pin di output del filtro PushSource. È anche possibile caricare e connettere i video di compressione, gli effetti video e così via.

> [!Note]  
> Il filtro di acquisizione desktop non supporta le sovrimpressione hardware, quindi non acquisisce il video sottoposto a rendering su una superficie di sovrapposizione o i cursori visualizzati tramite la sovrapposizione hardware. Usa GDI per convertire l'immagine desktop corrente in una bitmap, che viene passata al pin di output come esempio multimediale.

 

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: *\[ SDK \] Root* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ PushSource.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



