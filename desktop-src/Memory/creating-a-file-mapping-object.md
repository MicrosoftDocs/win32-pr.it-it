---
description: Il primo passaggio per eseguire il mapping di un file consiste nell'aprire il file chiamando la funzione CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Creazione di un oggetto di mapping dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65badc2af8aed5211c2f5c590fc0998019dae264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345366"
---
# <a name="creating-a-file-mapping-object"></a>Creazione di un oggetto di mapping dei file

Il primo passaggio per eseguire il mapping di un file consiste nell'aprire il file chiamando la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Per assicurarsi che altri processi non possano scrivere nella parte del file di cui è stato eseguito il mapping, è necessario aprire il file con accesso esclusivo. Inoltre, l'handle di file deve rimanere aperto fino a quando il processo non necessita più dell'oggetto mapping dei file. Un modo semplice per ottenere l'accesso esclusivo consiste nello specificare zero nel parametro *fdwShareMode* di **CreateFile**. L'handle restituito da **CreateFile** viene usato dalla funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare un oggetto mapping di file.

La funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) restituisce un handle per l'oggetto mapping del file. Questo handle verrà usato durante [la creazione di una visualizzazione file](creating-a-file-view.md) in modo da poter accedere alla memoria condivisa. Quando si chiama **CreateFileMapping**, si specifica il nome di un oggetto, il numero di byte da mappare dal file e l'autorizzazione di lettura/scrittura per la memoria mappata. Il primo processo che chiama **CreateFileMapping** crea l'oggetto mapping dei file. I processi che chiamano **CreateFileMapping** per un oggetto esistente ricevono un handle per l'oggetto esistente. È possibile stabilire se una chiamata a **CreateFileMapping** è stata creata o meno con esito positivo oppure se è stato aperto l'oggetto di mapping dei file chiamando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . **GetLastError** **non restituisce alcun \_ errore** al processo di creazione e l' **errore \_ \_ esiste già** nei processi successivi.

La funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) ha esito negativo se i flag di accesso sono in conflitto con quelli specificati quando la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) ha aperto il file. Ad esempio, per leggere e scrivere nel file:

-   Specificare i valori **generici di \_ lettura** e **\_ scrittura** generici nel parametro *fdwAccess* di [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   Specificare il **valore \_ ReadWrite della pagina** nel parametro *fdwProtect* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga).

La creazione di un oggetto mapping di file non esegue il commit della memoria fisica, ma la riserva.

## <a name="file-mapping-size"></a>Dimensioni del mapping dei file

Le dimensioni dell'oggetto mapping dei file sono indipendenti dalle dimensioni del file di cui è in corso il mapping. Tuttavia, se l'oggetto di mapping dei file è più grande del file, il sistema espande il file prima che [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) restituisca. Se l'oggetto di mapping dei file è più piccolo del file, il sistema esegue il mapping solo del numero specificato di byte dal file.

I parametri *dwMaximumSizeHigh* e *dwMaximumSizeLow* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) consentono di specificare il numero di byte da mappare dal file:

-   Quando non si desidera modificare le dimensioni del file (ad esempio, quando si esegue il mapping di file di sola lettura), chiamare [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) e specificare zero sia per *DwMaximumSizeHigh* che per *dwMaximumSizeLow*. In questo modo viene creato un oggetto mapping di file esattamente della stessa dimensione del file. In caso contrario, è necessario calcolare o stimare la dimensione del file finito perché gli oggetti di mapping dei file sono statici di dimensioni. una volta create, le dimensioni non possono essere aumentate o diminuite. Il tentativo di eseguire il mapping di un file con una lunghezza pari a zero in questo modo ha esito negativo e non è **\_ \_ valido** un codice di errore del file degli errori. I programmi devono verificare la presenza di file con una lunghezza pari a zero e rifiutare tali file.

-   Le dimensioni di un oggetto mapping di file supportato da un file denominato sono limitate dallo spazio su disco. Le dimensioni di una visualizzazione file sono limitate al blocco contiguo più grande disponibile di memoria virtuale non riservata. Si tratta di un massimo di 2 GB meno la memoria virtuale già riservata dal processo.

Le dimensioni dell'oggetto mapping dei file selezionato controllano la distanza del file che è possibile "visualizzare" con il mapping della memoria. Se si crea un oggetto di mapping dei file di 500 KB, è possibile accedere solo ai primi 500 KB del file, indipendentemente dalle dimensioni del file. Poiché non sono previste risorse di sistema per la creazione di un oggetto di mapping dei file più ampio, creare un oggetto mapping file che corrisponde alla dimensione del file (impostare i parametri *dwMaximumSizeHigh* e *dwMaximumSizeLow* di [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) entrambi su zero) anche se non si prevede di visualizzare l'intero file. Il costo delle risorse di sistema è quello di creare le visualizzazioni e accedervi.

Se si desidera visualizzare una parte del file che non si avvia all'inizio del file, è necessario creare un oggetto mapping di file. Questo oggetto corrisponde alla dimensione della parte del file che si desidera visualizzare più l'offset nel file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una vista in un file](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
