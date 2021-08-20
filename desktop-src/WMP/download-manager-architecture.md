---
title: Architettura di Download Manager
description: Architettura di Download Manager
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player online store, Download Manager
- negozi online, Download Manager
- Store online di tipo 2, Download Manager
- Windows Media Player,Download Manager
- Windows Media Player Download Manager
- Download Manager
- architettura per Download Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae04be86d935f87202abe4b0bf73e833a9da07cf89526b9dcb60de31eb881a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997101"
---
# <a name="download-manager-architecture"></a>Architettura di Download Manager

Il Windows Media Player Download Manager usa la tecnologia COM. La funzionalità viene trasformata in un set di interfacce di programmazione. È possibile scrivere codice di programmazione che usa queste interfacce usando Microsoft JScript o C++.

I linguaggi di scripting usano il concetto di oggetti per dividere la funzionalità di programmazione. Il **modello a oggetti DownloadManager** usa diversi oggetti per dividere i metodi e le proprietà in un'organizzazione logica che raggruppa funzioni semanticamente correlate. Le sezioni seguenti contengono informazioni sugli oggetti di Download Manager.



| Sezione                                                                     | Descrizione                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Informazioni sull'oggetto DownloadManager](#about-the-downloadmanager-object)       | **L'oggetto DownloadManager** rappresenta l'oggetto radice per l'Windows Media Player Download Manager. |
| [Informazioni sull'oggetto DownloadCollection](#about-the-downloadcollection-object) | **L'oggetto DownloadCollection** rappresenta una raccolta di elementi di download.                             |
| [Informazioni sull'oggetto DownloadItem](#about-the-downloaditem-object)             | **L'oggetto DownloadItem** rappresenta una singola richiesta di download.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Informazioni sull'oggetto DownloadManager

**DownloadManager** è l'oggetto radice per l'Windows Media Player Download Manager. Tutti gli altri oggetti sono accessibili tramite questo oggetto . Per ottenere l'accesso **all'oggetto DownloadManager,** usare la JScript seguente:


```C++
var DownloadManager = external.DownloadManager;
```



Verrà creata un'istanza **dell'oggetto DownloadManager,** che potrà quindi essere usata per recuperare gli oggetti figlio. Ad esempio, la sintassi seguente recupera il primo elemento dalla raccolta di download con il numero ID 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Informazioni sull'oggetto DownloadCollection

**L'oggetto DownloadCollection** rappresenta una raccolta di file da scaricare. È possibile usare questo oggetto per determinare il numero di download nella raccolta, rimuovere elementi dalla raccolta, recuperare un elemento di download specifico e avviare un nuovo download. L'avvio di un nuovo download aggiunge automaticamente il download alla raccolta.

## <a name="about-the-downloaditem-object"></a>Informazioni sull'oggetto DownloadItem

**L'oggetto DownloadItem** rappresenta un singolo download. Gli elementi di download esistono sempre come parte di una raccolta di download. Usare questo oggetto per recuperare informazioni sull'elemento di download e sospendere, riprendere o annullare il download in corso.

Quando si annulla un download, l'elemento di download rimane nella raccolta di download. In questo caso, **downloadCollection**. **downloadState** recupera il valore 4, ovvero annullato.

È possibile usare **downloadItem**. **stato** di avanzamento per informare l'utente sulla quantità di file trasferita o su quanto rimane da scaricare. È possibile usare questo valore per stimare anche il tempo rimanente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Download Manager**](download-manager.md)
</dt> </dl>

 

 




