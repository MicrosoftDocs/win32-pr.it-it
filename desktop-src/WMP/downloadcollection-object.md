---
title: Oggetto DownloadCollection
description: Oggetto DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player negozi online, oggetto DownloadCollection
- negozi online,oggetto DownloadCollection
- Tipo 2 negozi online, oggetto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902021"
---
# <a name="downloadcollection-object"></a>Oggetto DownloadCollection

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'oggetto DownloadCollection** contiene proprietà e metodi per gestire raccolte di elementi di download. Può essere usato dalle pagine Web ospitate in modalità completa Windows Media Player e che hanno accesso all'oggetto **Esterno,** ad esempio negozi online.

**L'oggetto DownloadCollection** supporta le proprietà seguenti.



| Proprietà                              | Descrizione                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Recupera il numero di download in sospeso.   |
| [id](downloadcollection-id.md)       | Recupera l'ID della raccolta di download. |



 

**L'oggetto DownloadCollection** supporta i metodi seguenti.



| Metodo                                                | Descrizione                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Cancella](downloadcollection-clear.md)                 | Rimuove tutti gli elementi da una raccolta di download. |
| [item](downloadcollection-item.md)                   | Recupera un oggetto di download in sospeso.          |
| [Removeitem](downloadcollection-removeitem.md)       | Rimuove un elemento di download da una raccolta.    |
| [startDownload](downloadcollection-startdownload.md) | Accoda un download.                            |



 

**L'oggetto DownloadCollection** è accessibile tramite i metodi seguenti.



| Oggetto                                        | Metodo                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

A scopo illustrativo, **DownloadManager**. **getDownloadCollection**(*collectionId*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




