---
description: Nell'esempio di codice SearchEvents viene illustrato come classificare in ordine di priorità gli eventi di indicizzazione.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306142"
---
# <a name="searchevents"></a>SearchEvents

Nell'esempio di codice SearchEvents viene illustrato come classificare in ordine di priorità gli eventi di indicizzazione.

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
| GitHub        | [Esempio SearchEvents](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Esplora risorse e passare alla directory del progetto **SearchEvents** .
2. Fare doppio clic sull'icona del file Eventing. sln per aprire il progetto in Visual Studio.
  
    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non avrà alcun effetto sul comportamento dell'esempio.

3. Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2. Al prompt dei comandi, immettere `Eventing.exe` o da Esplora risorse, fare doppio clic sull'icona per Eventing.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**livello di priorità \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**\_ITEMSTATE ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**\_tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
