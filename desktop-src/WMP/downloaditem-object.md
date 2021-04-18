---
title: Oggetto DownloadItem
description: Oggetto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online Stores, oggetto DownloadItem
- archivi online, oggetto DownloadItem
- digitare 2 archivi online, oggetto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298927"
---
# <a name="downloaditem-object"></a>Oggetto DownloadItem

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'oggetto **DownloadItem** rappresenta una richiesta di download del file. Può essere usato da pagine Web ospitate in modalità Full Windows Media Player e che hanno accesso all'oggetto **esterno** , ad esempio servizi Premium.

L'oggetto **DownloadItem** supporta le proprietà seguenti.



| Proprietà                                        | Descrizione                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Recupera lo stato del download.             |
| [corso](downloaditem-progress.md)           | Recupera lo stato di avanzamento del download in byte. |
| [size](downloaditem-size.md)                   | Recupera le dimensioni del download.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera l'URL di origine del download.        |
| [type](downloaditem-type.md)                   | Recupera il tipo di download.              |



 

L'oggetto **DownloadItem** supporta i metodi seguenti.



| Metodo                                      | Descrizione                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Annulla il download.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera il valore di un attributo per l'elemento di download. |
| [pause](downloaditem-pause.md)             | Sospende il download.                                       |
| [riprendere](downloaditem-resume.md)           | Riprende il download.                                      |



 

È possibile accedere all'oggetto **DownloadItem** tramite la proprietà seguente.



| Oggetto                                              | Proprietà                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Ai fini dell'illustrazione, **downloadmanager**. **Getdownloadcollection**(*CollectionId*). **Item**(*ItemId*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




