---
description: Per eseguire il mapping dei dati da un file alla memoria virtuale di un processo, è necessario creare una visualizzazione del file.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Creazione di una visualizzazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eadae741e9f74e8a3e1cd68006100d6acf82aad5019a8d31b18a7761c5620b69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067881"
---
# <a name="creating-a-file-view"></a>Creazione di una visualizzazione file

Per eseguire il mapping dei dati da un file alla memoria virtuale di un processo, è necessario creare una visualizzazione del file. Le [**funzioni MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) usano l'handle dell'oggetto di mapping dei file restituito da [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare una visualizzazione del file o di una parte del file nello spazio degli indirizzi virtuali del processo. Queste funzioni hanno esito negativo se i flag di accesso sono in conflitto con quelli specificati quando **CreateFileMapping ha** creato l'oggetto mapping file.

La [**funzione MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) restituisce un puntatore alla visualizzazione file. Dereferenziando un puntatore nell'intervallo di indirizzi specificato in **MapViewOfFile,** un'applicazione può leggere i dati dal file e scrivere dati nel file. La scrittura nella visualizzazione file comporta modifiche all'oggetto mapping file. La scrittura effettiva nel file su disco viene gestita dal sistema. I dati non vengono effettivamente trasferiti al momento della scrittura dell'oggetto di mapping dei file. Gran parte dell'input e dell'output del file (I/O) viene invece memorizzata nella cache per migliorare le prestazioni generali del sistema. Le applicazioni possono eseguire l'override di questo comportamento chiamando la [**funzione FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) per forzare il sistema a eseguire immediatamente transazioni su disco.

La [**funzione MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) funziona esattamente come la funzione [**MapViewOfFile,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) con la differenza che consente a un processo di specificare l'indirizzo di base della visualizzazione del file nello spazio degli indirizzi virtuali del processo nel *parametro lpvBase.* Se non è disponibile spazio sufficiente nell'indirizzo specificato, la chiamata ha esito negativo. Pertanto, se è necessario eseguire il mapping di un file allo stesso indirizzo in più processi, i processi devono negoziare un indirizzo appropriato: il *parametro lpvBase* deve essere un multiplo integrale della granularità di allocazione della memoria di sistema o la chiamata ha esito negativo. Per ottenere la granularità di allocazione di memoria del sistema, usare la [**funzione GetSystemInfo,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) che compila i membri di una [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

Un'applicazione può creare più visualizzazioni file dallo stesso oggetto di mapping dei file. Una visualizzazione file può avere dimensioni diverse rispetto all'oggetto mapping file da cui deriva, ma deve essere inferiore all'oggetto mapping file. L'offset specificato dai *parametri dwOffsetHigh* e *dwOffsetLow* di [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) deve essere un multiplo della granularità di allocazione del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una vista all'interno di un file](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
