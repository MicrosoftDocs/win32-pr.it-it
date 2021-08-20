---
description: Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla funzione MapViewOfFile, come illustrato negli esempi seguenti.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lettura e scrittura da una visualizzazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee56f1d06e53bdfd6f7571e4ec296da0270ce0a7050b253b5900c4640d6df0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067681"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lettura e scrittura da una visualizzazione file

Per leggere da una visualizzazione file, dereferenziare il puntatore restituito dalla [**funzione MapViewOfFile,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) come illustrato negli esempi seguenti.

La lettura o la scrittura in una visualizzazione file di un file diverso dal file di pagina può causare un'eccezione **EXCEPTION \_ IN PAGE \_ \_ ERROR.** Ad esempio, l'accesso a un file mappato che risiede in un server remoto può generare un'eccezione se la connessione al server viene persa. Le eccezioni possono verificarsi anche a causa di un disco completo, di un errore del dispositivo sottostante o di un errore di allocazione della memoria. Quando si scrive in una visualizzazione file, possono verificarsi eccezioni anche perché il file è condiviso e un processo diverso ha bloccato un intervallo di byte. Per proteggersi dalle eccezioni dovute a errori di input e output (I/O), tutti i tentativi di accedere ai file mappati alla memoria devono essere incapsulati in gestori eccezioni strutturate. Quando si riceve **EXCEPTION \_ IN PAGE \_ \_ ERROR** nel filtro **\_ \_ tranne** , assicurarsi che l'indirizzo sia all'interno del mapping a cui si sta accedendo. In tal caso, eseguire il ripristino o l'esito negativo correttamente. In caso contrario, non gestire l'eccezione.

L'esempio seguente usa il puntatore restituito **da MapViewOfFile** per leggere dalla visualizzazione file:


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



Nell'esempio seguente viene utilizzato il puntatore restituito **da MapViewOfFile** per scrivere nella visualizzazione file:


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



La [**funzione FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia il numero specificato di byte della visualizzazione file nel file fisico, senza attendere l'esecuzione dell'operazione di scrittura memorizzata nella cache:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Se si esegue il mapping di un file compresso o di tipo sparse in una partizione NTFS, è possibile che si sia verificato un errore di I/O durante il paging in una parte del file. In questo caso, lo spazio indirizzi mappato da [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) potrebbe non essere supportato dallo spazio su disco allocato. Questo perché un file di tipo sparse può avere aree con zeri per cui NTFS non alloca spazio su disco e un file compresso può richiedere meno spazio su disco rispetto ai dati effettivi che rappresenta. Se si legge o si scrive in una parte di un file di tipo sparse o compresso che non è supportato dallo spazio su disco, il sistema operativo potrebbe tentare di allocare spazio su disco. Se il disco è pieno, può verificarsi un'eccezione che indica un errore di I/O.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle eccezioni strutturata](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
