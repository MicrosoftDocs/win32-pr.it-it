---
description: Per creare una libreria di Dynamic-Link (DLL), è necessario creare uno o più file di codice sorgente ed eventualmente un file del linker per l'esportazione delle funzioni.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Creazione della libreria di Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753778"
---
# <a name="dynamic-link-library-creation"></a>Creazione della libreria di Dynamic-Link

Per creare una libreria di Dynamic-Link (DLL), è necessario creare uno o più file di codice sorgente ed eventualmente un file del linker per l'esportazione delle funzioni. Se si prevede di consentire alle applicazioni che utilizzano la DLL di utilizzare il collegamento dinamico in fase di caricamento, è necessario creare anche una libreria di importazione.

## <a name="creating-source-files"></a>Creazione di file di origine

I file di origine per una DLL contengono funzioni e dati esportati, funzioni e dati interni e una [funzione del punto di ingresso](dynamic-link-library-entry-point-function.md) facoltativa per la dll. È possibile utilizzare qualsiasi strumento di sviluppo che supporta la creazione di DLL basate su Windows.

Se la DLL può essere usata da un'applicazione multithreading, è consigliabile rendere la DLL "thread-safe". Per evitare il danneggiamento dei dati, è necessario sincronizzare l'accesso a tutti i dati globali della DLL. È inoltre necessario assicurarsi di collegare solo le librerie thread-safe. Ad esempio, Microsoft Visual C++ contiene più versioni della libreria di runtime del linguaggio C, una non thread-safe e due.

## <a name="exporting-functions"></a>Esportazione di funzioni

Il modo in cui si specificano le funzioni in una DLL da esportare dipende dagli strumenti utilizzati per lo sviluppo. Alcuni compilatori consentono di esportare una funzione direttamente nel codice sorgente usando un modificatore nella dichiarazione di funzione. In altri casi, è necessario specificare le esportazioni in un file passato al linker.

Ad esempio, usando Visual C++, esistono due modi possibili per esportare le funzioni DLL: con il modificatore [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) o con un file di definizione moduli (con estensione def). Se si usa il modificatore **\_ \_ declspec (dllexport)** , non è necessario usare un file def. Per ulteriori informazioni, vedere [esportazione da una dll](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Creazione di una libreria di importazione

Un file della libreria di importazione (lib) contiene informazioni necessarie al linker per risolvere i riferimenti esterni alle funzioni DLL esportate, in modo che il sistema possa individuare la DLL specificata e le funzioni DLL esportate in fase di esecuzione. Quando si compila la DLL, è possibile creare una libreria di importazione per la DLL.

Per ulteriori informazioni, vedere [compilazione di una libreria di importazione e di un file di esportazione](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Utilizzo di una libreria di importazione

Per chiamare la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) , ad esempio, è necessario collegare il codice alla libreria di importazione User32. lib. Il motivo è che **CreateWindow** risiede in una DLL di sistema denominata User32.dll e User32. lib è la libreria di importazione usata per risolvere le chiamate alle funzioni esportate in User32.dll nel codice. Il linker crea una tabella che contiene l'indirizzo di ogni chiamata di funzione. Le chiamate alle funzioni in una DLL verranno corrette quando viene caricata la DLL. Durante l'inizializzazione del processo, il sistema carica User32.dll perché il processo dipende dalle funzioni esportate in tale DLL e aggiorna le voci nella tabella dell'indirizzo della funzione. Tutte le chiamate a **CreateWindow** richiamano la funzione esportata da User32.dll.

Per informazioni, vedere [collegamento implicito a una dll](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una libreria a collegamento dinamico semplice](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[Dll (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
