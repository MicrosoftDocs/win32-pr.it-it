---
title: Oggetto DownloadItem
description: Oggetto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player store online, oggetto DownloadItem
- negozi online, oggetto DownloadItem
- tipo 2 negozi online, oggetto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfea6241e81352b8848304c3601650ef4dec2a8e5692874fa20995ccddcce38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863461"
---
# <a name="downloaditem-object"></a>Oggetto DownloadItem

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

**L'oggetto DownloadItem** rappresenta una richiesta di download di file. Può essere usato dalle pagine Web ospitate nella modalità completa Windows Media Player e  che hanno accesso all'oggetto Esterno, ad esempio i servizi Premium.

**L'oggetto DownloadItem** supporta le proprietà seguenti.



| Proprietà                                        | Descrizione                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Recupera lo stato del download.             |
| [Progresso](downloaditem-progress.md)           | Recupera lo stato di avanzamento del download in byte. |
| [size](downloaditem-size.md)                   | Recupera le dimensioni del download.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera l'URL di origine del download.        |
| [type](downloaditem-type.md)                   | Recupera il tipo di download.              |



 

**L'oggetto DownloadItem** supporta i metodi seguenti.



| Metodo                                      | Descrizione                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Annulla il download.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera il valore di un attributo per l'elemento di download. |
| [pause](downloaditem-pause.md)             | Sospende il download.                                       |
| [riassumere](downloaditem-resume.md)           | Riprende il download.                                      |



 

È possibile accedere all'oggetto **DownloadItem** tramite la proprietà seguente.



| Oggetto                                              | Proprietà                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

A scopo illustrativo, **DownloadManager**. **getDownloadCollection**(*collectionId*). **item**(*itemId*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




