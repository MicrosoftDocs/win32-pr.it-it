---
title: Stato della cache nella radice di virtualizzazione
description: Descrive i diversi Stati della cache che un file o una directory gestita dal provider può avere.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 43d62ceb1f5ef5bf07000666f336077270b1e86a
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/22/2020
ms.locfileid: "104398433"
---
# <a name="cache-state-in-the-virtualization-root"></a>Stato della cache nella radice di virtualizzazione

Il provider usa il file system locale sotto la radice di virtualizzazione come una cache degli elementi gestiti.  Un elemento (file o directory) può trovarsi in uno dei sei Stati del file system locale:

* Le macchine

  L'elemento non esiste localmente sul disco.  Viene proiettata, ad esempio sintetizzata, durante le enumerazioni della relativa directory padre.  Gli elementi virtuali vengono uniti con tutti gli elementi che possono esistere sul disco per presentare il contenuto completo della directory padre.

* Segnaposto

  Per i file: il contenuto del file (flusso di dati primario) non è presente sul disco.  I metadati del file (nome, dimensioni, timestamp, attributi e così via) vengono memorizzati nella cache del disco.
  
  Per le directory: alcuni o tutti i discendenti immediati della directory (i file e le directory nella directory) non sono presenti sul disco, ovvero sono ancora virtuali.  I metadati della directory (nome, timestamp, attributi e così via) vengono memorizzati nella cache del disco.

* Segnaposto idrato

  Per i file: il contenuto e i metadati del file sono stati memorizzati nella cache sul disco.  Definito anche "file parziale".
  
  Per le directory: una directory creata su disco come segnaposto non diventa mai una directory di segnaposto idratata.  In questo modo, il provider può aggiungere o rimuovere elementi dalla directory nell'archivio di backup e fare in modo che tali modifiche vengano riflesse nella cache locale.

* Segnaposto Dirty (idrato o meno)

  I metadati dell'elemento sono stati modificati localmente e non è più una cache dello stato nell'archivio del provider. Si noti che la creazione o l'eliminazione di un file o di una directory in una directory segnaposto fa sì che la directory segnaposto diventi Dirty.

* File/directory completa

  Per i file: il contenuto del file (flusso di dati primario) è stato modificato.  Il file non è più una cache dello stato nell'archivio del provider.  Anche i file che sono stati creati nel file system locale (ovvero che non esistono nell'archivio del provider) sono considerati file completi.
  
  Per le directory: le directory che sono state create nel file system locale (ovvero che non esistono nell'archivio del provider) sono considerate directory complete.  Una directory creata su disco come segnaposto non diventa mai una directory completa.
  
* Rimozione definitiva

  Segnaposto nascosto speciale che rappresenta un elemento eliminato dalla file system locale.  Quando una directory viene enumerata ProjFS unisce il set di elementi locali (segnaposto, file completi e così via) con il set di elementi proiettati virtuali.  Se un elemento viene visualizzato sia nei set locali che in quelli proiettati, l'elemento locale ha la precedenza.  Se un file non esiste nel file system locale, non esiste alcuno stato locale, quindi verrebbe visualizzato nell'enumerazione.  Tuttavia, se l'elemento è stato eliminato, la relativa visualizzazione nell'enumerazione risulterebbe imprevista.  La sostituzione di un elemento eliminato con un oggetto contrassegnato per la rimozione definitiva comporta gli effetti seguenti:

  * Enumerazioni per non rivelare l'elemento.
  * Si apre un file che prevede che l'elemento esista, ad esempio "file non trovato".
  * Creazione di file che prevede la riuscita solo se l'elemento non esiste correttamente; ProjFS rimuove l'oggetto contrassegnato per la rimozione definitiva come parte dell'operazione.

Per illustrare gli stati precedenti, considerare la sequenza seguente, dato un provider ProjFS con un singolo file "foo.txt" situato nella radice di virtualizzazione C:\Root.

1. Un'app enumera C:\Root.  Viene visualizzato il file virtuale "foo.txt".  Poiché non è ancora stato eseguito l'accesso al file, il file non esiste sul disco.
1. L'app apre un handle per C:\root\foo.txt.  ProjFS indica al provider di creare un segnaposto.
1. L'app legge il contenuto del file.  Il provider fornisce il contenuto del file a ProjFS e viene memorizzato nella cache per C:\root\foo.txt.  Il file è ora un segnaposto idrato.
1. L'app Aggiorna il timestamp dell'Ultima modifica.  Il file è ora un segnaposto Dirty idratato.
1. L'app apre un handle per l'accesso in scrittura al file.  C:\root\foo.txt ora è un file completo.
1. L'app Elimina C:\root\foo.txt.  ProjFS sostituisce il file con un oggetto contrassegnato per la rimozione definitiva.  A questo punto, quando l'app enumera c: root, non viene visualizzato foo.txt.  Se tenta di aprire il file, l'apertura ha esito negativo con ERROR_FILE_NOT_FOUND.
