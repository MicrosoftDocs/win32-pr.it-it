---
description: L'esempio di codice StructuredQuerySample illustra come leggere righe dalla console, analizzarle usando lo schema di sistema e visualizzare gli alberi delle condizioni risultanti.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab8f32a3ed58133893ed5c38c16c2ac242e9a28c6384a4e354bb6b0524c5a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462576"
---
# <a name="structuredquerysample"></a>StructuredQuerySample

L'esempio di codice StructuredQuerySample illustra come leggere righe dalla console, analizzarle usando lo schema di sistema e visualizzare gli alberi delle condizioni risultanti.

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
| GitHub        | [StructuredQuerySample](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

## <a name="building-the-sample"></a>Compilazione dell'esempio

1. Aprire Windows Explorer e passare alla directory **del progetto StructuredQuerySample.**
2. Fare doppio clic sull'icona per il file StructuredQuerySample.sln per aprire il progetto in Visual Studio.

    > [!NOTE]  
    > Il file sln è stato creato con una versione precedente di Visual Studio, pertanto sarà necessario aggiornarlo se si esegue Visual Studio 2012 o versione successiva. Ciò non inciderà sul comportamento dell'esempio.

3. Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1. Passare alla directory che contiene il nuovo eseguibile usando la finestra del prompt dei comandi o Windows Explorer.
2. Al prompt dei comandi immettere o in Windows Explorer fare doppio clic `StructuredQuerySample.exe` sull'icona per StructuredQuerySample.exe.

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[**IQueryParserManager**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a>Altri esempi

[Esempi di codice di ricerca](-search-samples-ovw.md)
