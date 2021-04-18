---
description: Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306148"
---
# <a name="crawlscopecommandline"></a>CrawlScopeCommandLine

Nell'esempio di codice CrawlScopeCommandLine viene illustrato come definire le opzioni della riga di comando per le operazioni di indicizzazione di gestione dell'ambito di ricerca (CSM).

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

| Location | Percorso o URL                                                                |
|----------|----------------------------------------------------------------------------|
| GitHub   |    [Esempio CrawlScopeCommandLine](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Esplora risorse e passare alla directory del progetto **CrawlScopeCommandLine** .
2. Fare doppio clic sull'icona per il file csmcmd. sln per aprire il progetto in Visual Studio.
  
    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non avrà alcun effetto sul comportamento dell'esempio.

3. Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2. Al prompt dei comandi, immettere `csmcmd.exe` o da Esplora risorse, fare doppio clic sull'icona per csmcmd.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
