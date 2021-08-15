---
description: L'esempio di codice IFilterSample illustra come creare una classe di base IFilter per l'implementazione dell'interfaccia IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f015166d0366152d07a5fb8d182edcb5422112c66f016219970fef9b889df3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863734"
---
# <a name="ifiltersample"></a>IFilterSample

L'esempio di codice IFilterSample illustra come creare una classe di base IFilter per l'implementazione [**dell'interfaccia IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)

In questo argomento sono contenute le sezioni seguenti.

- [Requisiti](#requirements)
- [Download dell'esempio](#downloading-the-sample)
- [Compilazione dell'esempio](#building-the-sample)
- [Esecuzione dell'esempio](#running-the-sample)
- [Argomenti correlati](#related-topics)

## <a name="requirements"></a>Requisiti

| Prodotto     | Versione prodotto          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 o 10    |
| Windows SDK | 7.0 o versione successiva           |

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel percorso seguente.

| Località      | URL del percorso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Windows Explorer e passare alla directory **del progetto FilterBase.**
2. Fare doppio clic sull'icona del file FilterBase.sln per aprire il progetto in Visual Studio.

    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, pertanto sarà necessario aggiornarlo se si esegue Visual Studio 2012 o versione successiva. Ciò non inciderà sul comportamento dell'esempio.

3. Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory che contiene il nuovo eseguibile, usando la finestra del prompt dei comandi o Windows Explorer.
2. Al prompt dei comandi immettere o in Windows Explorer fare doppio clic `FilterBase.exe` sull'icona per FilterBase.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Informazioni concettuali

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
