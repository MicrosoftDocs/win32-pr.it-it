---
description: Esempio di filtri di origine push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Esempio di filtri di origine push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521330"
---
# <a name="push-source-filters-sample"></a>Esempio di filtri di origine push

## <a name="description"></a>Descrizione

Questo esempio è costituito da un set di tre filtri di origine che forniscono i dati di origine seguenti come flusso video:

-   CPushSourceBitmap: singola bitmap (caricata dalla directory corrente)
-   CPushSourceBitmapSet: set di bitmap (caricato dalla directory corrente)
-   CPushSourceDesktop: copia dell'immagine desktop corrente (solo GDI)

## <a name="usage"></a>Utilizzo

Per usare un filtro, caricarlo in GraphEdit ed eseguirne il rendering del PIN di output. Questo consentirà di connettere un renderer video (e possibilmente un filtro del convertitore dello spazio colore) e di visualizzare l'output. Se si vuole eseguire il rendering dell'output in un file AVI, caricare il mux di file AVI, caricare un filtro del writer di file, specificare un nome di output per il writer di file ed eseguire il rendering del PIN di output del filtro PushSource. È anche possibile caricare e connettere i commediatori video, gli effetti video e così via.

> [!Note]  
> Il filtro di acquisizione desktop non supporta le sovrapposizioni hardware, quindi non acquisisce il rendering del video in una superficie sovrapposta o i cursori visualizzati tramite la sovrapposizione hardware. USA GDI per convertire l'immagine desktop corrente in una bitmap, che viene passata al pin di output come esempio multimediale.

 

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ PushSource.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



