---
title: Oggetto indexer
description: Oggetto indexer
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK, oggetti indicizzatore
- Advanced Systems Format (ASF), oggetti indicizzatore
- ASF (Advanced Systems Format),oggetti indicizzatore
- oggetti,oggetti indicizzatore
- oggetti indicizzatore
- indici, oggetti indicizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795ef166f6b3ad46897305cbd3f6c38bbc7a219bb99df1dcf8b14dbfb1443577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839788"
---
# <a name="indexer-object"></a>Oggetto indexer

L'oggetto indicizzatore crea un indice in un file ASF. Un indice è una parte standard di un file ASF che equivale a campioni video con orari, numeri di fotogrammi o (se applicabile) indicatori di ora standard SMPTE (Society of Motion Picture and Television Engineers). Senza un indice, né l'oggetto lettore né l'oggetto lettore sincrono possono cercare un punto al centro di un file.

Gli indici creati da questo oggetto sono necessari solo se il file contiene uno o più flussi video. Ciò è dovuto al fatto che i dati audio non vengono compressi a livello temporale, rendendo più semplice trovare un determinato tempo in un flusso audio.

L'oggetto indicizzatore viene creato dalla [**funzione WMCreateIndexer,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) che imposta un puntatore a **un'interfaccia IWMIndexer.** Le altre interfacce dell'oggetto indicizzatore possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto indicizzatore.



| Interfaccia                          | Descrizione                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Avvia e arresta il processo di indicizzazione.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configura l'indicizzatore, abilitando l'indicizzazione in base al frame, al tempo o tramite SMPTE time code. |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter usare l'oggetto indicizzatore.



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




