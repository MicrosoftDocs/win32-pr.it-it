---
description: L'esempio di codice DSearch illustra come creare una classe per un'applicazione console statica per eseguire query Windows Search usando l'assembly Microsoft.Search.Interop per ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2505a8482a698f3147ae9c13ddb135c1da1c584f16cf52a5a05ca469efbc968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680713"
---
# <a name="dsearch"></a>DSearch

L'esempio di codice DSearch illustra come creare una classe per un'applicazione console statica per eseguire query Windows Search usando l'assembly Microsoft.Search.Interop per [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).

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

| Località      | URL percorso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Esempio di DSearch](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> Per tutte le versioni di Windows, Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Windows Explorer e passare alla directory **del progetto DSearch.**
2. Fare doppio clic sull'icona per il file DSearch.sln per aprire il progetto in Visual Studio.
  
    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non influisce sul comportamento dell'esempio.

3. Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory che contiene il nuovo eseguibile usando la finestra del prompt dei comandi o Windows Explorer.
2. Al prompt dei comandi immettere o da esplora Windows fare doppio clic `DSearch.exe` sull'icona per DSearch.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
