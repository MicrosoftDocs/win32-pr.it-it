---
description: Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, USA le informazioni inserite dal linker nel file per individuare i nomi delle DLL utilizzate dal processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Collegamento dinamico Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530013"
---
# <a name="load-time-dynamic-linking"></a>Collegamento dinamico Load-Time

Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, USA le informazioni inserite dal linker nel file per individuare i nomi delle DLL utilizzate dal processo. Il sistema cerca quindi le dll. Per ulteriori informazioni, vedere l' [ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md).

Se il sistema non è in grado di individuare una DLL obbligatoria, termina il processo e visualizza una finestra di dialogo che segnala l'errore all'utente. In caso contrario, il sistema esegue il mapping della DLL allo spazio degli indirizzi virtuali del processo e incrementa il conteggio dei riferimenti alla DLL.

Il sistema chiama la funzione del punto di ingresso. La funzione riceve un codice che indica che il processo sta caricando la DLL. Se la funzione del punto di ingresso non restituisce TRUE, il sistema termina il processo e segnala l'errore. Per ulteriori informazioni sulla funzione del punto di ingresso, vedere [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Infine, il sistema modifica la tabella degli indirizzi di funzione con gli indirizzi iniziali per le funzioni DLL importate.

La DLL viene mappata allo spazio degli indirizzi virtuali del processo durante l'inizializzazione e viene caricata nella memoria fisica solo quando necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Load-Time collegamento dinamico](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



