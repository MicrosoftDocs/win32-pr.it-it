---
description: Il primo passaggio per eseguire il mapping di un file consiste nell'aprire il file chiamando la funzione CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Creazione di un oggetto mapping file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502c484dd0466b47a87f4db205d1da5499bf5ef
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432503"
---
# <a name="creating-a-file-mapping-object"></a>Creazione di un oggetto mapping file

Il primo passaggio per eseguire il mapping di un file consiste nell'aprire il file chiamando la [**funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea) Per assicurarsi che altri processi non siano in grado di scrivere nella parte del file di cui è stato eseguito il mapping, è necessario aprire il file con accesso esclusivo. Inoltre, l'handle di file deve rimanere aperto fino a quando il processo non richiede più l'oggetto mapping file. Un modo semplice per ottenere l'accesso esclusivo è specificare zero nel parametro *fdwShareMode* di **CreateFile**. L'handle restituito **da CreateFile** viene usato dalla [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare un oggetto di mapping dei file.

La [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) restituisce un handle per l'oggetto mapping di file. Questo handle verrà usato durante la [creazione di una visualizzazione file](creating-a-file-view.md) in modo da poter accedere alla memoria condivisa. Quando si chiama **CreateFileMapping**, si specifica un nome di oggetto, il numero di byte di cui eseguire il mapping dal file e l'autorizzazione di lettura/scrittura per la memoria mappata. Il primo processo che chiama **CreateFileMapping crea** l'oggetto mapping file. I processi che chiamano **CreateFileMapping** per un oggetto esistente ricevono un handle per l'oggetto esistente. È possibile stabilire se una chiamata a **CreateFileMapping** ha creato o aperto l'oggetto mapping di file chiamando la [**funzione GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **GetLastError** restituisce **NO \_ ERROR** al processo di creazione e **ERROR ALREADY \_ \_ EXISTS** per i processi successivi.

La [**funzione CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) ha esito negativo se i flag di accesso sono in conflitto con quelli specificati quando la [**funzione CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) ha aperto il file. Ad esempio, per leggere e scrivere nel file:

-   Specificare i **\_ valori GENERIC READ** **e GENERIC \_ WRITE** nel parametro *fdwAccess* di [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   Specificare il **valore PAGE \_ READWRITE** nel parametro *fdwProtect* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga).

La creazione di un oggetto mapping di file non esegue il commit della memoria fisica, ma la riserva.

## <a name="file-mapping-size"></a>Dimensioni mapping file

Le dimensioni dell'oggetto mapping file sono indipendenti dalle dimensioni del file di cui viene eseguito il mapping. Tuttavia, se l'oggetto di mapping dei file è più grande del file, il sistema espande il file prima che [**venga restituito CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) Se l'oggetto mapping file è più piccolo del file, il sistema esegue il mapping solo al numero specificato di byte dal file.

I *parametri dwMaximumSizeHigh* e *dwMaximumSizeLow* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) consentono di specificare il numero di byte di cui eseguire il mapping dal file:

-   Quando non si desidera modificare le dimensioni del file , ad esempio quando si esegue il mapping di file di sola lettura, chiamare [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) e specificare zero per *dwMaximumSizeHigh* e *dwMaximumSizeLow*. In questo modo viene creato un oggetto di mapping dei file che ha esattamente le stesse dimensioni del file. In caso contrario, è necessario calcolare o stimare le dimensioni del file completato perché le dimensioni degli oggetti di mapping dei file sono statiche. Dopo la creazione, le dimensioni non possono essere aumentate o ridotte. Un tentativo di eseguire il mapping di un file con una lunghezza pari a zero in questo modo ha esito negativo e il codice di errore **è \_ ERROR FILE \_ INVALID**. I programmi devono testare i file con lunghezza zero e rifiutare tali file.

-   Le dimensioni di un oggetto mapping file supportato da un file denominato sono limitate dallo spazio su disco. Le dimensioni di una visualizzazione file sono limitate al blocco contiguo più grande disponibile di memoria virtuale non riservata. Si tratta al massimo di 2 GB meno la memoria virtuale già riservata dal processo.

Le dimensioni dell'oggetto di mapping dei file selezionato controllano la distanza nel file che è possibile "vedere" con il mapping della memoria. Se si crea un oggetto mapping di file di dimensioni di 500 Kb, si ha accesso solo ai primi 500 Kb del file, indipendentemente dalle dimensioni del file. Poiché non sono necessarie risorse di sistema per creare un oggetto di mapping dei file di dimensioni maggiori, creare un oggetto di mapping file con le dimensioni del file (impostare i parametri *dwMaximumSizeHigh* e *dwMaximumSizeLow* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) entrambi su zero) anche se non si prevede di visualizzare l'intero file. Il costo delle risorse di sistema deriva dalla creazione delle viste e dall'accesso.

È possibile visualizzare una parte del file che non inizia all'inizio del file. Per altre informazioni, vedere [Creazione di una vista all'interno di un file](creating-a-view-within-a-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>
[Creazione di una vista file Creazione](creating-a-file-view.md)
</dt> di una vista <dt> 
[all'interno di un file](creating-a-view-within-a-file.md)
</dt> </dl>


 
