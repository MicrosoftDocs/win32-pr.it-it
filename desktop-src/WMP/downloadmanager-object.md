---
title: Oggetto DownloadManager
description: Oggetto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online Stores, oggetto DownloadManager
- archivi online, oggetto DownloadManager
- digitare 2 archivi online, oggetto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856346"
---
# <a name="downloadmanager-object"></a>Oggetto DownloadManager

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'oggetto **downloadmanager** è l'oggetto radice per gestione download di Windows Media Player. Può essere usato da pagine Web ospitate nei riquadri attività del servizio di archiviazione online.

L'oggetto **downloadmanager** supporta i metodi seguenti.



| Metodo                                                                   | Descrizione                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crea una raccolta di download vuota.        |
| [getdownloadcollection](downloadmanager-getdownloadcollection.md)       | Recupera la raccolta di download specificata. |



 

È possibile accedere all'oggetto **downloadmanager** tramite **External. DownloadManager**. A scopo illustrativo, si presuppone che questo valore sia stato assegnato a una variabile denominata "DownloadManager", che verrà usata per identificare questo oggetto nelle sezioni della sintassi di riferimento.

In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **downloadmanager** sono accessibili solo dai riquadri attività del servizio di archiviazione online. Non è possibile usare **downloadmanager** da altre funzionalità in cui l'oggetto **esterno** è disponibile, ad esempio HtmlView, visualizzazione centro informazioni e informazioni sugli album.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




