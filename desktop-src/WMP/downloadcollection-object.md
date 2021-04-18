---
title: Download (oggetto)
description: Download (oggetto)
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Online Stores, oggetto DownloadCollection
- archivi online, oggetto DownloadCollection
- digitare 2 archivi online, oggetto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298533"
---
# <a name="downloadcollection-object"></a>Download (oggetto)

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'oggetto **DownloadCollection** contiene proprietà e metodi per gestire le raccolte di elementi di download. Può essere usato da pagine Web ospitate in modalità Full Windows Media Player e che hanno accesso all'oggetto **esterno** , ad esempio gli archivi online.

L'oggetto **DownloadCollection** supporta le proprietà seguenti.



| Proprietà                              | Descrizione                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Recupera il numero di download in sospeso.   |
| [id](downloadcollection-id.md)       | Recupera l'ID della raccolta di download. |



 

L'oggetto **DownloadCollection** supporta i metodi seguenti.



| Metodo                                                | Descrizione                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Cancella](downloadcollection-clear.md)                 | Rimuove tutti gli elementi da una raccolta di download. |
| [item](downloadcollection-item.md)                   | Recupera un oggetto di download in sospeso.          |
| [removeItem](downloadcollection-removeitem.md)       | Rimuove un elemento di download da una raccolta.    |
| [startDownload](downloadcollection-startdownload.md) | Accoda un download.                            |



 

È possibile accedere all'oggetto **DownloadCollection** tramite i metodi seguenti.



| Oggetto                                        | Metodo                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getdownloadcollection](downloadmanager-getdownloadcollection.md)       |



 

Ai fini dell'illustrazione, **downloadmanager**. **Getdownloadcollection**(*CollectionId*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




