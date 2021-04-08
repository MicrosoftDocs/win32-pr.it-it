---
description: Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch potrebbe richiedere l'accesso all'origine dell'installazione originale.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedire a una patch di richiedere l'accesso all'origine di installazione originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881030"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedire a una patch di richiedere l'accesso all'origine di installazione originale

Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch potrebbe richiedere l'accesso all'origine dell'installazione originale.

Attenersi ai punti seguenti per ridurre al minimo la possibilità che la patch richieda l'accesso all'origine originale:

-   Utilizzare patch con solo file completi. In questo modo si elimina la necessità di creare patch binarie per tutte le versioni rilasciate in precedenza del file. Si noti che le dimensioni dell'intero file sono in genere maggiori delle patch binarie. È possibile impostare in modo semplice una patch per l'intero file creando la proprietà IncludeWholeFilesOnly con un valore di 1 (uno) nel file della patch Creation Properties (PCP).
-   Assicurarsi che nessuna delle azioni personalizzate acceda al percorso di origine originale.
-   Verificare che l'azione ResolveSource sia condizionata in modo che venga eseguita solo quando necessario o in alternativa non è presente.
-   Popolare la [tabella MsiFileHash](msifilehash-table.md) per tutti i file non con versione. Lo strumento Windows Installer SDK Msifiler.exe consente di eseguire facilmente questa operazione.
-   Verificare che tutti i file dispongano delle informazioni corrette sulla versione e sulla lingua. Lo strumento Windows Installer SDK Msifiler.exe consente di eseguire facilmente questa operazione.

## <a name="source-requirements-when-patching"></a>Requisiti di origine per l'applicazione di patch

L'accesso alle origini di installazione originali potrebbe essere necessario per applicare la patch nei casi seguenti:

-   La patch si applica a una funzionalità attualmente eseguita dall'origine. In questo caso, la funzionalità viene passata dallo stato di esecuzione dall'origine allo stato locale.
-   La patch si applica a un componente con un file mancante o danneggiato.
-   La patch si applica a un file in un componente che contiene anche file senza versione senza voci MsiFileHash. Una [tabella MsiFileHash](msifilehash-table.md) popolata è necessaria per evitare la Ricopia non necessaria dei file non con versione dal percorso di origine.
-   La patch è stata applicata con un REINSTALLMODE di divertimenti o emù. Questa opzione è pericolosa perché esegue operazioni di copia dei file indipendentemente dalla versione del file. Ciò può compromettere la riesecuzione dei file e richiede quasi sempre l'origine. Il valore REINSTALLMODE consigliato è omus.
-   Il pacchetto memorizzato nella cache per il prodotto è mancante. Il pacchetto memorizzato nella cache è necessario per l'applicazione di una patch. Il pacchetto memorizzato nella cache è archiviato nella cartella% windir% \\ Installer.
-   Il pacchetto viene creato per effettuare una chiamata all' [azione ResolveSource](resolvesource-action.md). Questa azione dovrebbe in genere essere evitata o condizionata in modo appropriato, perché la sua esecuzione comporta sempre l'accesso all'origine.
-   Il pacchetto ha un'azione personalizzata che tenta di accedere all'origine in qualche modo. L'esempio più comune è un'azione personalizzata di tipo 23 installazione simultanea.
    > [!Note]  
    > Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).

     

-   Il pacchetto di patch è costituito da patch binarie che non si applicano alla versione corrente del file nel computer.

Si consideri l'esempio seguente, in cui Windows Installer richiede l'accesso all'origine originale quando si applica una patch:

1.  Installare la versione RTM dell'esempio del prodotto.
2.  Applicare la patch Qfe1. msp al computer. Questa patch versione 1,0 di Example.dll alla versione 1,1.
3.  Viene fornita una nuova patch, Qfe2. msp, che aggiorna Example.dll alla versione 1,2 e obsolete Qfe1. msp. Tuttavia, la patch è stata creata solo per la versione 1,0 di Example.dll perché è stata generata con la versione RTM del prodotto. Example.dll versione 1,2 include la correzione contenuta nella versione 1,1 Example.dll, ma il file con estensione msp è stato generato tra le immagini RTM e QFE2. Quindi, quando Qfe2. msp viene applicato al computer, Windows Installer necessario accedere all'origine originale. La patch binaria per Example.dll non può essere applicata alla versione 1,1; può essere applicato solo alla versione 1,0. In questo modo il programma di installazione ricopiando la versione 1,0 di Example.dll dal percorso di origine originale, in modo che la patch possa essere applicata correttamente.

## <a name="source-requirements-when-removing-a-patch"></a>Requisiti di origine per la rimozione di una patch

Potrebbe essere necessario accedere alle origini di installazione originali per rimuovere una patch se il Windows Installer non ha archiviato le informazioni di base sulla patch. A partire da Windows Installer 3,0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornate. Per altre informazioni sulla cache di base, vedere [riduzione delle dimensioni delle patch](reducing-patch-size.md) .

 

 



