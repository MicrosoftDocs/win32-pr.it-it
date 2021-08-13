---
description: Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, usa le informazioni inserite dal linker nel file per individuare i nomi delle DLL usate dal processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0adac32841d822bba67031dd79171c52f25d8308b055aee2c55bb804ebefe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649359"
---
# <a name="load-time-dynamic-linking"></a>Load-Time collegamento dinamico

Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, usa le informazioni inserite dal linker nel file per individuare i nomi delle DLL usate dal processo. Il sistema cerca quindi le DLL. Per altre informazioni, vedere [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

Se il sistema non riesce a individuare una DLL necessaria, termina il processo e visualizza una finestra di dialogo che segnala l'errore all'utente. In caso contrario, il sistema esegue il mapping della DLL nello spazio degli indirizzi virtuali del processo e incrementa il conteggio dei riferimenti dll.

Il sistema chiama la funzione del punto di ingresso. La funzione riceve un codice che indica che il processo sta caricando la DLL. Se la funzione del punto di ingresso non restituisce TRUE, il sistema termina il processo e segnala l'errore. Per altre informazioni sulla funzione del punto di ingresso, vedere [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Infine, il sistema modifica la tabella degli indirizzi delle funzioni con gli indirizzi iniziali per le funzioni DLL importate.

La DLL viene mappata nello spazio degli indirizzi virtuali del processo durante l'inizializzazione e viene caricata nella memoria fisica solo quando necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso Load-Time collegamento dinamico](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



