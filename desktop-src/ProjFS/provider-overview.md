---
title: Panoramica del provider
description: Panoramica concettuale di un'applicazione provider.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474800"
---
# <a name="provider-overview"></a>Panoramica del provider

Il provider è un'applicazione in modalità utente che gestisce e riconosce un archivio dati di supporto.  Il provider implementa i callback ProjFS e usa l'API ProjFS per proiettare questo archivio dati nel file system in cui viene visualizzato all'utente come file e directory.  L'archivio di backup del provider può essere locale nel sistema dell'utente oppure potrebbe trovarsi in modalità remota.

## <a name="data-projection"></a>Proiezione dati

La parte del file system di proprietà del provider, in cui vengono proiettati i dati, è radicata in una directory denominata "radice di virtualizzazione".  Quando il provider vuole iniziare a proiettare i dati, avvia una "istanza di virtualizzazione", ovvero un oggetto che gestisce la comunicazione tra il provider e ProjFS per il set di file e directory che si trovano in una particolare radice di virtualizzazione.  Tutti i file e le directory discendenti dalla radice di virtualizzazione che non sono stati creati localmente dall'utente vengono materializzati dal provider tramite l'API ProjFS.  Questi elementi iniziano come file e directory virtuali, ovvero non esistono nel dispositivo di archiviazione locale dell'utente, ma vengono inseriti in risultati di enumerazione per ProjFS.  Quando gli elementi vengono aperti e letti, ProjFS richiama i callback implementati dal provider per richiedere i dati e il provider usa le API ProjFS per inviare i dati alla risorsa di archiviazione locale in cui viene memorizzata nella cache per l'accesso successivo.  Se è necessario modificare la visualizzazione dell'archivio dati di supporto, ad esempio se il contenuto dell'archivio dati è stato modificato, il provider può utilizzare le API ProjFS per aggiornare o eliminare gli elementi locali in modo da riflettere la nuova visualizzazione dell'archivio dati.

## <a name="callback-return-codes"></a>Codici restituiti di callback

Ogni callback elenca un numero di possibili valori restituiti specifici di tale callback.  Oltre ai valori restituiti elencati per un determinato callback, un callback può restituire anche altri codici di errore.  Si tratta dell'elenco completo dei codici di errore che possono essere restituiti da un callback:

| Codice di errore                                    | Significato
|-----------------------------------------------|--------
| S_OK                                          | Operazione riuscita
| E_OUTOFMEMORY                                 | Non è stato possibile allocare la memoria necessaria.
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)          | Il provider desidera completare l'operazione in un secondo momento.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Un buffer passato a un callback è troppo piccolo.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | Il file non esiste nell'archivio di backup del provider.
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)   | Un argomento di callback non è valido.  Ad esempio, un ID di enumerazione non corrisponde a una sessione di enumerazione attiva.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | Il provider desidera impedire l'esecuzione di un'operazione, ad esempio una ridenominazione o un'eliminazione.

I callback possono inoltre restituire eventuali errori che possono ricevere dalle chiamate alle API ProjFS.
Se un callback restituisce un codice di errore non presente nell'elenco precedente o che non proviene da un'API ProjFS, ProjFS lo restituirà al file system come STATUS_INTERNAL_ERROR.
