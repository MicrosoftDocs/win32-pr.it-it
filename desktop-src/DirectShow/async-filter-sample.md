---
description: Esempio di filtro asincrono
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Esempio di filtro asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049048"
---
# <a name="async-filter-sample"></a>Esempio di filtro asincrono

## <a name="description"></a>Descrizione

L'esempio di filtro asincrono è un filtro di lettura file che supporta il download progressivo. Questo filtro di esempio implementa le interfacce [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) . Supporta i file MPEG, ma non i file AVI.

## <a name="usage"></a>Utilizzo

Questo esempio include una piccola applicazione della riga di comando, Memfile.exe, che illustra il filtro. Gli argomenti della riga di comando specificano un file multimediale e una velocità in bit, espressa in kilobyte al secondo. L'applicazione legge il file in memoria alla velocità specificata e riproduce il file. A tale scopo, viene creata un'istanza del filtro, viene aggiunto il filtro al grafo del filtro ed eseguito il rendering del PIN di output del filtro.

Dalla riga di comando digitare:

**Velocità in bit del file Memfile**  

Il filtro di esempio asincrono non supporta i file AVI, perché non è in grado di connettersi al filtro del [separatore AVI](avi-splitter-filter.md) . Il pin di output del filtro asincrono propone MEDIATYPE \_ Stream e MEDIASUBTYPE \_ null per il tipo di supporto. Il pin di input nel filtro di separatore AVI non accetta MEDIASUBTYPE \_ null e non propone alcun tipo. Pertanto, la connessione al pin ha esito negativo. Il filtro asincrono potrebbe essere migliorato per offrire MEDIASUBTYPE \_ AVI quando appropriato. Ad esempio, potrebbe esaminare il formato di file o usare l'estensione di file.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: \[ *SDK radice* \] \\ esempi di \\ \\ filtri DirectShow \\ multimediali \\ Async.

## <a name="related-topics"></a>Argomenti correlati



[Esempi di DirectShow](directshow-samples.md)


 

 



