---
title: Architettura di Download Manager
description: Architettura di Download Manager
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- architettura per Download Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708560"
---
# <a name="download-manager-architecture"></a>Architettura di Download Manager

Gestione download di Windows Media Player utilizza la tecnologia COM. La funzionalità è distillata in un set di interfacce di programmazione; è possibile scrivere codice di programmazione che utilizza queste interfacce utilizzando Microsoft JScript o C++.

I linguaggi di scripting utilizzano il concetto di oggetti per dividere la funzionalità di programmazione. Il modello a oggetti **downloadmanager** utilizza diversi oggetti per dividere i metodi e le proprietà in un'organizzazione logica che raggruppa le funzioni semanticamente correlate. Le sezioni seguenti contengono informazioni sugli oggetti di Download Manager.



| Sezione                                                                     | Descrizione                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Informazioni sull'oggetto DownloadManager](#about-the-downloadmanager-object)       | L'oggetto **downloadmanager** rappresenta l'oggetto radice per gestione download di Windows Media Player. |
| [Informazioni sull'oggetto DownloadCollection](#about-the-downloadcollection-object) | L'oggetto **DownloadCollection** rappresenta una raccolta di elementi di download.                             |
| [Informazioni sull'oggetto DownloadItem](#about-the-downloaditem-object)             | L'oggetto **DownloadItem** rappresenta una singola richiesta di download.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Informazioni sull'oggetto DownloadManager

**Downloadmanager** è l'oggetto radice per gestione download di Windows Media Player. Tutti gli altri oggetti sono accessibili tramite questo oggetto. Per ottenere l'accesso all'oggetto **downloadmanager** , usare la sintassi JScript seguente:


```C++
var DownloadManager = external.DownloadManager;
```



In questo modo viene creata un'istanza dell'oggetto **downloadmanager** , che può quindi essere utilizzata per recuperare gli oggetti figlio. La sintassi seguente, ad esempio, recupera il primo elemento dalla raccolta di download con ID numero 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Informazioni sull'oggetto DownloadCollection

L'oggetto **DownloadCollection** rappresenta una raccolta di file da scaricare. È possibile utilizzare questo oggetto per determinare il numero di download nella raccolta, rimuovere gli elementi dalla raccolta, recuperare un elemento di download specifico e avviare un nuovo download. Quando si avvia un nuovo download, il download viene aggiunto automaticamente alla raccolta.

## <a name="about-the-downloaditem-object"></a>Informazioni sull'oggetto DownloadItem

L'oggetto **DownloadItem** rappresenta un singolo download. Gli elementi di download sono sempre presenti come parte di una raccolta di download. Utilizzare questo oggetto per recuperare informazioni sull'elemento di download e per sospendere, riprendere o annullare il download in corso.

Quando si annulla un download, l'elemento di download rimane sul posto nella relativa raccolta di download. In questo caso, **scaricarecollection**. **downloadState** recupera un valore pari a 4, ovvero annullato.

È possibile usare **downloadItem**. stato di **avanzamento** per informare l'utente sulla quantità di file trasferiti o su quanto resta da scaricare. È possibile utilizzare questo valore per stimare anche il tempo rimanente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione download**](download-manager.md)
</dt> </dl>

 

 




