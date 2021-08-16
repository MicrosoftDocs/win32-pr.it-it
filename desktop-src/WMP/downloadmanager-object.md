---
title: Oggetto DownloadManager
description: Oggetto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player negozi online, oggetto DownloadManager
- negozi online,oggetto DownloadManager
- Tipo 2 negozi online, oggetto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 500061e414d7321ed6fe4c46cafc79cd6795935847bb3d8c527364497722ecf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340525"
---
# <a name="downloadmanager-object"></a>Oggetto DownloadManager

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'oggetto DownloadManager** è l'oggetto radice per Windows Media Player Download Manager. Può essere usato dalle pagine Web ospitate nei riquadri attività del servizio negozio online.

**L'oggetto DownloadManager** supporta i metodi seguenti.



| Metodo                                                                   | Descrizione                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crea una raccolta di download vuota.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Recupera la raccolta di download specificata. |



 

È **possibile accedere all'oggetto DownloadManager** usando **external. DownloadManager**. A scopo illustrativo, si presuppone che questo valore sia stato assegnato a una variabile denominata "DownloadManager", che verrà usata per identificare questo oggetto nelle sezioni della sintassi di riferimento.

In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **DownloadManager** sono accessibili solo dai riquadri attività del servizio negozio online. Non è possibile usare **DownloadManager** da altre funzionalità in cui è disponibile l'oggetto **External,** ad esempio HTMLView, la visualizzazione Info Center e le informazioni sugli album.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




