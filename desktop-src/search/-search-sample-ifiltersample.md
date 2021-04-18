---
description: Nell'esempio di codice IFilterSample viene illustrato come creare una classe di base IFilter per implementare l'interfaccia IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306146"
---
# <a name="ifiltersample"></a>IFilterSample

Nell'esempio di codice IFilterSample viene illustrato come creare una classe di base IFilter per implementare l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

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
| Windows SDK | 7,0 o versione successiva           |

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel percorso seguente.

| Location      | URL percorso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [IFilterSample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Esplora risorse e passare alla directory del progetto **FilterBase** .
2. Fare doppio clic sull'icona per il file FilterBase. sln per aprire il progetto in Visual Studio.

    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non avrà alcun effetto sul comportamento dell'esempio.

3. Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2. Al prompt dei comandi, immettere `FilterBase.exe` o da Esplora risorse, fare doppio clic sull'icona per FilterBase.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a>Informazioni concettuali

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
