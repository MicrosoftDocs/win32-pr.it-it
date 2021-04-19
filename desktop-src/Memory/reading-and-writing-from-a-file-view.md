---
description: Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla funzione MapViewOfFile, come illustrato negli esempi seguenti.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lettura e scrittura da una visualizzazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319445"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lettura e scrittura da una visualizzazione file

Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , come illustrato negli esempi seguenti.

La lettura o la scrittura in una visualizzazione file di un file diverso dal file di paging può causare un'eccezione in un'eccezione **\_ di \_ \_ errore di pagina** . Se ad esempio si accede a un file mappato che risiede in un server remoto, è possibile che venga generata un'eccezione in caso di perdita della connessione al server. Le eccezioni possono anche verificarsi a causa di un disco completo, di un errore di dispositivo sottostante o di un errore di allocazione della memoria. Quando si scrive in una visualizzazione file, le eccezioni possono anche verificarsi perché il file è condiviso e un altro processo ha bloccato un intervallo di byte. Per evitare eccezioni a causa di errori di input e output (I/O), tutti i tentativi di accesso ai file mappati alla memoria devono essere racchiusi in gestori di eccezioni strutturate. Quando si riceve **un' \_ eccezione \_ nell' \_ errore di pagina** nel filtro **\_ \_ ad eccezione** , assicurarsi che l'indirizzo sia incluso nel mapping a cui si sta effettuando l'accesso. In tal caso, ripristinare o non riuscire normalmente; in caso contrario, non gestire l'eccezione.

Nell'esempio seguente viene usato il puntatore restituito da **MapViewOfFile** per leggere dalla visualizzazione file:


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



Nell'esempio seguente viene usato il puntatore restituito da **MapViewOfFile** per scrivere nella visualizzazione file:


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



La funzione [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia il numero specificato di byte della visualizzazione file nel file fisico, senza attendere che si verifichi l'operazione di scrittura memorizzata nella cache:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Se si esegue il mapping di un file compresso o sparse in una partizione NTFS, è possibile che si verifichi un errore di I/O durante il paging in una parte del file. In questo caso, lo spazio degli indirizzi mappato da [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) potrebbe non essere supportato dallo spazio su disco allocato. Ciò è dovuto al fatto che un file sparse può avere aree di zero per le quali NTFS non alloca spazio su disco e un file compresso può richiedere meno spazio su disco rispetto ai dati effettivi che rappresenta. Se si leggono o si scrive in una parte di un file sparse o compresso non supportato da spazio su disco, il sistema operativo potrebbe tentare di allocare spazio su disco. Se il disco è pieno, è possibile che venga generata un'eccezione che indica un errore di I/O.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione strutturata delle eccezioni](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
