---
description: Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch può richiedere l'accesso all'origine di installazione originale.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedire a una patch di richiedere l'accesso all'origine di installazione originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5dcadae12b733d76dee8c3acd5ec6af6169c47cfd8c7eeb22ad9693a75859a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376790"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedire a una patch di richiedere l'accesso all'origine di installazione originale

Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch può richiedere l'accesso all'origine di installazione originale.

Attenersi ai punti seguenti per ridurre al minimo la possibilità che la patch richieda l'accesso all'origine originale:

-   Usare patch solo per file interi. Ciò elimina la necessità di creare patch binarie per tutte le versioni rilasciate in precedenza del file. Si noti che le patch di file intere hanno in genere dimensioni maggiori rispetto alle patch binarie. È possibile impostare facilmente una patch in modo che sia un'intera patch di file tramite la creazione della proprietà IncludeWholeFilesOnly con un valore pari a 1 (uno) nel file Delle proprietà di creazione patch (PCP).
-   Assicurarsi che nessuna delle azioni personalizzate accerta l'accesso al percorso di origine originale.
-   Assicurarsi che l'azione ResolveSource sia condizionata in modo che venga eseguita solo quando necessario o in alternativa non sia presente.
-   Popolare la tabella [MsiFileHash per](msifilehash-table.md) tutti i file senza versione. Lo Windows SDK del programma di installazione, Msifiler.exe, può eseguire facilmente questa operazione.
-   Assicurarsi che tutti i file siano con le informazioni corrette sulla versione e sulla lingua. Lo Windows SDK del programma di installazione, Msifiler.exe, può eseguire facilmente questa operazione.

## <a name="source-requirements-when-patching"></a>Requisiti di origine per l'applicazione di patch

Potrebbe essere necessario accedere alle origini di installazione originali per applicare la patch nei casi seguenti:

-   La patch si applica a una funzionalità attualmente in esecuzione dall'origine. In questo caso, la funzionalità viene passata dallo stato run-from-source allo stato locale.
-   La patch si applica a un componente con un file mancante o danneggiato.
-   La patch si applica a un file in un componente che contiene anche file senza versione senza voci MsiFileHash. È necessaria [una tabella MsiFileHash](msifilehash-table.md) popolata per impedire la ricopia non necessaria dei file non versioneti dal percorso di origine.
-   La patch è stata applicata con REINSTALLMODE di amus o emus. Questa opzione è pericolosa in quanto esegue operazioni di copia di file indipendentemente dalla versione del file. Ciò può causare il down-reving dei file e quasi sempre richiede l'origine. Il valore REINSTALLMODE consigliato è omus.
-   Il pacchetto memorizzato nella cache per il prodotto è mancante. Il pacchetto memorizzato nella cache è necessario per l'applicazione di una patch. Il pacchetto memorizzato nella cache viene archiviato nella cartella %windir% \\ Installer.
-   Il pacchetto viene creato per eseguire una chiamata [all'azione ResolveSource](resolvesource-action.md). Questa azione deve in genere essere evitata o condizionata in modo appropriato, perché la relativa esecuzione comporta sempre un accesso all'origine.
-   Il pacchetto ha un'azione personalizzata che tenta di accedere all'origine in qualche modo. L'esempio più comune è un'azione personalizzata di installazione simultanea di tipo 23.
    > [!Note]  
    > Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [Installazioni simultanee](concurrent-installations.md).

     

-   Il pacchetto di patch è costituito da patch binarie che non si applicano alla versione corrente del file nel computer.

Si consideri l'esempio seguente Windows programma di installazione richiede l'accesso all'origine originale quando si applica una patch:

1.  Installare la versione RTM del prodotto Esempio.
2.  Applicare la patch Qfe1.msp al computer. Questa patch è la versione 1.0 Example.dll alla versione 1.1.
3.  Viene fornita una nuova patch, Qfe2.msp, che Example.dll alla versione 1.2 e obsoleta Qfe1.msp. Tuttavia, la patch è stata creata solo per la versione 1.0 di Example.dll perché è stata generata usando la versione RTM del prodotto. Example.dll versione 1.2 include la correzione contenuta in Example.dll versione 1.1, ma il file msp è stato generato tra le immagini RTM e QFE2. Pertanto, quando Qfe2.msp viene applicato al computer, Windows installer deve accedere all'origine originale. La patch binaria per Example.dll non può essere applicata alla versione 1.1. può essere applicato solo alla versione 1.0. In questo modo, il programma di installazione ricopia la versione 1.0 Example.dll dal percorso di origine originale in modo che la patch possa essere applicata correttamente.

## <a name="source-requirements-when-removing-a-patch"></a>Requisiti di origine durante la rimozione di una patch

L'accesso alle origini di installazione originali potrebbe essere necessario per rimuovere una patch se il programma di installazione Windows non ha archiviato le informazioni di base sulla patch. A partire da Windows Installer 3.0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornati. Per altre informazioni sulla cache di base, vedere [Riduzione delle dimensioni delle patch.](reducing-patch-size.md)

 

 



