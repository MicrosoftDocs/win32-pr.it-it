---
description: L'esempio di codice SearchEvents illustra come assegnare priorità agli eventi di indicizzazione.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: Eventi di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f6687de8a9e4816968a3134abf76f8b10e02f42d90a2578626be035843621c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969710"
---
# <a name="searchevents"></a>Eventi di ricerca

L'esempio di codice SearchEvents illustra come assegnare priorità agli eventi di indicizzazione.

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
| GitHub        | [Esempio di SearchEvents](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Per tutte le versioni di Windows, Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Windows Explorer e passare alla directory del progetto **SearchEvents.**
2. Fare doppio clic sull'icona per il file Eventing.sln per aprire il progetto in Visual Studio.
  
    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non influisce sul comportamento dell'esempio.

3. Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory che contiene il nuovo eseguibile usando la finestra del prompt dei comandi o Windows Explorer.
2. Al prompt dei comandi immettere o in Esplora Windows fare doppio clic `Eventing.exe` sull'icona per Eventing.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**LIVELLO DI \_ PRIORITÀ**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**TIPO \_ ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
