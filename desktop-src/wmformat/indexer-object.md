---
title: Oggetto indicizzatore
description: Oggetto indicizzatore
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK, oggetti indicizzatore
- ASF (Advanced Systems Format), oggetti indicizzatore
- ASF (formato avanzato dei sistemi), oggetti indicizzatore
- oggetti, oggetti indicizzatore
- oggetti indicizzatore
- indici, oggetti indicizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104046421"
---
# <a name="indexer-object"></a>Oggetto indicizzatore

L'oggetto indicizzatore crea un indice in un file ASF. Un indice è una parte standard di un file ASF che equivale a campionamenti video con orari, numeri di frame o (se applicabile) la società dei timestamp standard di Motion Picture and Television Engineers (SMPTE). Senza un indice, né l'oggetto Reader né l'oggetto Reader sincrono possono cercare in un punto all'interno di un file.

Gli indici creati da questo oggetto sono necessari solo se il file contiene uno o più flussi video. Questo perché i dati audio non vengono compressi temporaneamente, semplificando l'individuazione di un determinato periodo di tempo in un flusso audio.

L'oggetto indicizzatore viene creato dalla funzione [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , che imposta un puntatore a un'interfaccia **IWMIndexer** . Le altre interfacce dell'oggetto indicizzatore possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto indicizzatore.



| Interfaccia                          | Descrizione                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Avvia e arresta il processo di indicizzazione.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configura l'indicizzatore, abilitando l'indicizzazione in base al frame, al tempo o al codice ora SMPTE. |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter usare l'oggetto indicizzatore.



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve i messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




