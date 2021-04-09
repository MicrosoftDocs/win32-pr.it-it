---
description: Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e la ricerca di Windows tramite Structured Query Language (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878805"
---
# <a name="wssql"></a>WSSQL

Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e la ricerca di Windows tramite Structured Query Language (SQL).

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
| GitHub        | [Esempio WSSQL](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Esplora risorse e passare alla directory del progetto **WSSQL** .
2. Fare doppio clic sull'icona per il file WSSQL. sln per aprire il progetto in Visual Studio.
    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, quindi l'aggiornamento sarà necessario se si esegue Visual Studio 2012 o versione successiva. Questo non avrà alcun effetto sul comportamento dell'esempio.

3. Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2. Al prompt dei comandi, immettere `WSSQL.exe` o da Esplora risorse, fare doppio clic sull'icona per WSSQL.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="conceptual"></a>Informazioni concettuali

[Uso della sintassi SQL di Windows Search](-search-sql-windowssearch-entry.md)

[Informazioni generali sul linguaggio di query](-search-sql-generalqueryinfo.md)

[Panoramica della programmazione OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
