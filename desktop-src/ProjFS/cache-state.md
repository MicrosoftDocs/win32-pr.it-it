---
title: Stato della cache nella radice di virtualizzazione
description: Descrive i diversi stati della cache che possono avere un file o una directory gestita dal provider.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 378973075017cc1ac06bf46840ea9d2d1058150a46587eb537374d501396ce30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792868"
---
# <a name="cache-state-in-the-virtualization-root"></a>Stato della cache nella radice di virtualizzazione

Il provider usa l'file system locale nella radice di virtualizzazione come cache degli elementi gestiti.  Un elemento (file o directory) può essere in uno dei sei stati del file system:

* Le macchine

  L'elemento non esiste in locale sul disco.  Viene proiettato, ad esempio sintetizzato, durante le enumerazioni della directory padre.  Gli elementi virtuali vengono uniti a tutti gli elementi che possono esistere su disco per presentare il contenuto completo della directory padre.

* Segnaposto

  Per i file: il contenuto del file (flusso di dati primario) non è presente sul disco.  I metadati del file (nome, dimensione, timestamp, attributi e così via) vengono memorizzati nella cache del disco.
  
  Per le directory: alcuni o tutti i discendenti immediati della directory (i file e le directory nella directory) non sono presenti sul disco, ovvero sono ancora virtuali.  I metadati della directory (nome, timestamp, attributi e così via) vengono memorizzati nella cache del disco.

* Segnaposto idrato

  Per i file: il contenuto e i metadati del file sono stati memorizzati nella cache sul disco.  Definito anche "file parziale".
  
  Per le directory: una directory creata su disco come segnaposto non diventa mai una directory segnaposto idrato.  In questo modo il provider può aggiungere o rimuovere elementi dalla directory nel relativo archivio di backup e fare in modo che tali modifiche siano riflesse nella cache locale.

* Segnaposto dirty (idratato o meno)

  I metadati dell'elemento sono stati modificati in locale e non sono più una cache del relativo stato nell'archivio del provider. Si noti che la creazione o l'eliminazione di un file o di una directory in una directory segnaposto causa lo dirty della directory segnaposto.

* File/directory completo

  Per i file: il contenuto del file (flusso di dati primario) è stato modificato.  Il file non è più una cache del relativo stato nell'archivio del provider.  Anche i file creati nel file system locale (ovvero che non esistono affatto nell'archivio del provider) vengono considerati file completi.
  
  Per le directory: le directory create nel file system locale (ovvero che non esistono affatto nell'archivio del provider) vengono considerate directory complete.  Una directory creata su disco come segnaposto non diventa mai una directory completa.
  
* Tombstone

  Segnaposto nascosto speciale che rappresenta un elemento eliminato dal file system.  Quando una directory viene enumerata, ProjFS unisce il set di elementi locali (segnaposto, file completi e così via) con il set di elementi proiettati virtuali.  Se un elemento viene visualizzato sia nei set locali che nei set proiettati, l'elemento locale ha la precedenza.  Se un file non esiste nell'file system non è presente alcuno stato locale, verrà quindi visualizzato nell'enumerazione .  Tuttavia, se l'elemento fosse stato eliminato, la visualizzazione nell'enumerazione sarebbe imprevista.  La sostituzione di un elemento eliminato con un oggetto contrassegnato per la rimozione definitiva comporta gli effetti seguenti:

  * Enumerazioni per non rivelare l'elemento.
  * L'apertura del file che prevede l'esistenza dell'elemento ha esito negativo, ad esempio "file non trovato".
  * Il file crea che prevedono l'esito positivo solo se l'elemento non esiste; ProjFS rimuove l'oggetto contrassegnato per la rimozione definitiva come parte dell'operazione.

Per illustrare gli stati precedenti, si consideri la sequenza seguente, dato un provider ProjFS con un singolo file "foo.txt" che si trova nella radice di virtualizzazione C:\root.

1. Un'app enumera C:\root.  Viene visualizzato il file virtuale "foo.txt".  Poiché non è ancora stato eseguito l'accesso al file, il file non esiste su disco.
1. L'app apre un handle per C:\root\foo.txt.  ProjFS indica al provider di creare un segnaposto.
1. L'app legge il contenuto del file.  Il provider fornisce il contenuto del file a ProjFS e viene memorizzato nella cache per C:\root\foo.txt.  Il file è ora un segnaposto idrato.
1. L'app aggiorna il timestamp dell'ultima modifica.  Il file è ora un segnaposto dirty hydrated.
1. L'app apre un handle per l'accesso in scrittura al file.  C:\root\foo.txt è ora un file completo.
1. L'app elimina C:\root\foo.txt.  ProjFS sostituisce il file con un oggetto contrassegnato per la rimozione definitiva.  Ora, quando l'app enumera C:\root, non visualizza foo.txt.  Se tenta di aprire il file, l'apertura non riesce con ERROR_FILE_NOT_FOUND.
