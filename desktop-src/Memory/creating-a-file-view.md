---
description: Per eseguire il mapping dei dati da un file alla memoria virtuale di un processo, è necessario creare una vista del file.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Creazione di una visualizzazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f7ba132efd9ecf82f9ec087492c9622824b51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967421"
---
# <a name="creating-a-file-view"></a>Creazione di una visualizzazione file

Per eseguire il mapping dei dati da un file alla memoria virtuale di un processo, è necessario creare una vista del file. Le funzioni [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) usano l'handle dell'oggetto di mapping dei file restituito da [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) per creare una visualizzazione del file o una parte del file nello spazio degli indirizzi virtuali del processo. Queste funzioni hanno esito negativo se i flag di accesso sono in conflitto con quelli specificati quando **CreateFileMapping** ha creato l'oggetto di mapping dei file.

La funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) restituisce un puntatore alla visualizzazione file. Dereferenziando un puntatore nell'intervallo di indirizzi specificato in **MapViewOfFile**, un'applicazione può leggere i dati dal file e scrivere i dati nel file. La scrittura nella visualizzazione file comporta modifiche all'oggetto mapping dei file. La scrittura effettiva nel file su disco viene gestita dal sistema. I dati non vengono effettivamente trasferiti nel momento in cui viene scritto l'oggetto di mapping dei file. Al contrario, gran parte dell'input e dell'output (I/O) del file viene memorizzata nella cache per migliorare le prestazioni generali del sistema. Le applicazioni possono eseguire l'override di questo comportamento chiamando la funzione [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) per forzare il sistema a eseguire immediatamente le transazioni disco.

La funzione [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) funziona esattamente come la funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) ad eccezione del fatto che consente a un processo di specificare l'indirizzo di base della vista del file nello spazio degli indirizzi virtuali del processo nel parametro *lpvBase* . Se non è disponibile spazio sufficiente nell'indirizzo specificato, la chiamata ha esito negativo. Pertanto, se è necessario eseguire il mapping di un file allo stesso indirizzo in più processi, i processi devono negoziare un indirizzo appropriato: il parametro *lpvBase* deve essere un multiplo integrale della granularità dell'allocazione di memoria di sistema o la chiamata non riesce. Per ottenere la granularità dell'allocazione di memoria del sistema, utilizzare la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) , che compila i membri di una struttura di [**\_ informazioni di sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

Un'applicazione può creare più visualizzazioni di file dallo stesso oggetto mapping di file. Una visualizzazione file può avere dimensioni diverse rispetto all'oggetto di mapping dei file da cui viene derivata, ma deve essere inferiore all'oggetto mapping di file. L'offset specificato dai parametri *dwOffsetHigh* e *dwOffsetLow* di [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) deve essere un multiplo della granularità di allocazione del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una vista in un file](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
