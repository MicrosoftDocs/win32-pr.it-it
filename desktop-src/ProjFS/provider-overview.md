---
title: Panoramica del provider
description: Panoramica concettuale di un'applicazione provider.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6905d6d2d52fd30b8950682c45c9d3bd0fc13281fc0f1d3120cba1b168012d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127961"
---
# <a name="provider-overview"></a>Panoramica del provider

Il provider è un'applicazione in modalità utente che gestisce e comprende un archivio dati di backup.  Il provider implementa i callback ProjFS e usa l'API ProjFS per proiettare questo archivio dati nell'file system dove viene visualizzato all'utente come file e directory.  L'archivio di backup del provider può essere locale nel sistema dell'utente o in remoto.

## <a name="data-projection"></a>Proiezione dei dati

La parte del file system di proprietà del provider, in cui vengono proiettati i dati, è radice in una directory denominata "radice di virtualizzazione".  Quando il provider vuole iniziare a proiettare i dati, avvia un'"istanza di virtualizzazione", ovvero un oggetto che gestisce la comunicazione tra il provider e ProjFS per il set di file e directory che si trovano in una determinata radice di virtualizzazione.  Tutti i file e le directory discendenti della radice di virtualizzazione che non sono stati creati localmente dall'utente vengono materializzati dal provider tramite l'API ProjFS.  Questi elementi iniziano come file e directory virtuali, ovvero non esistono nel dispositivo di archiviazione locale dell'utente, ma vengono inseriti nei risultati dell'enumerazione da ProjFS.  Quando gli elementi vengono aperti e letti, ProjFS richiama i callback implementati dal provider per richiedere i dati e il provider usa le API ProjFS per inviare i dati alla memoria locale in cui vengono memorizzati nella cache per l'accesso successivo.  Se è necessario modificare la visualizzazione dell'archivio dati di backup da parte dell'utente, ad esempio se il contenuto dell'archivio dati è stato modificato, il provider può usare le API ProjFS per aggiornare o eliminare elementi locali in modo da riflettere la nuova visualizzazione dell'archivio dati.

## <a name="callback-return-codes"></a>Codici restituiti di callback

Ogni callback elenca una serie di possibili valori restituiti specifici di tale callback.  Oltre ai valori restituiti elencati per un callback specificato, un callback può restituire anche altri codici di errore.  Questo è l'elenco completo dei codici di errore che possono essere restituiti da un callback:

| Codice di errore                                    | Significato
|-----------------------------------------------|--------
| S_OK                                          | Operazione completata
| E_OUTOFMEMORY                                 | Impossibile allocare la memoria necessaria.
| HRESULT_FROM_WIN32(ERROR_IO_PENDING)          | Il provider desidera completare l'operazione in un secondo momento.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Un buffer passato a un callback era troppo piccolo.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | Il file non esiste nell'archivio di backup del provider.
| HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)   | Un argomento di callback non è valido.  Ad esempio, un ID di enumerazione non corrisponde a una sessione di enumerazione attiva.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | Il provider desidera impedire l'esecuzione di un'operazione, ad esempio la ridenominazione o l'eliminazione.

I callback possono anche restituire eventuali errori che possono ricevere dalle chiamate alle API ProjFS.
Se un callback restituisce un codice di errore che non è nell'elenco precedente o che non deriva da un'API ProjFS, ProjFS lo restituirà al file system come STATUS_INTERNAL_ERROR.
