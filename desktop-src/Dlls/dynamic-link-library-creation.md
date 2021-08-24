---
description: Per creare una libreria Dynamic-Link (DLL), è necessario creare uno o più file di codice sorgente ed eventualmente un file del linker per l'esportazione delle funzioni.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89047e24fe61483b3ac807b59abc114206a00f9df18566b5fb02947268fbd792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650451"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link della libreria

Per creare una libreria Dynamic-Link (DLL), è necessario creare uno o più file di codice sorgente ed eventualmente un file del linker per l'esportazione delle funzioni. Se si prevede di consentire alle applicazioni che usano la DLL di usare il collegamento dinamico in fase di caricamento, è necessario creare anche una libreria di importazione.

## <a name="creating-source-files"></a>Creazione di file di origine

I file di origine per una DLL contengono funzioni e dati esportati, funzioni interne e dati e una funzione facoltativa del punto di [ingresso](dynamic-link-library-entry-point-function.md) per la DLL. È possibile usare qualsiasi strumento di sviluppo che supporti la creazione Windows DLL basate su codice.

Se la DLL può essere usata da un'applicazione multithreading, è necessario rendere la DLL "thread-safe". È necessario sincronizzare l'accesso a tutti i dati globali della DLL per evitare il danneggiamento dei dati. È anche necessario assicurarsi di collegarsi solo a librerie thread-safe. Ad esempio, Microsoft Visual C++ contiene più versioni della libreria di runtime C, una non thread-safe e due che lo sono.

## <a name="exporting-functions"></a>Esportazione di funzioni

Il modo in cui si specificano le funzioni in una DLL da esportare dipende dagli strumenti utilizzati per lo sviluppo. Alcuni compilatori consentono di esportare una funzione direttamente nel codice sorgente usando un modificatore nella dichiarazione di funzione. In altri casi, è necessario specificare le esportazioni in un file passato al linker.

Ad esempio, usando Visual C++, è possibile esportare le funzioni DLL in due modi: con il modificatore [**\_ \_ declspec(dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) o con un file di definizione del modulo (def). Se si usa il **\_ \_ modificatore declspec(dllexport),** non è necessario usare un file def. Per altre informazioni, vedere [Esportazione da una DLL.](/cpp/build/exporting-from-a-dll?view=vs-2019)

## <a name="creating-an-import-library"></a>Creazione di una libreria di importazione

Un file di libreria di importazione (con estensione lib) contiene informazioni necessarie al linker per risolvere i riferimenti esterni alle funzioni DLL esportate, in modo che il sistema possa individuare la DLL specificata e le funzioni DLL esportate in fase di esecuzione. È possibile creare una libreria di importazione per la DLL quando si compila la DLL.

Per altre informazioni, vedere [Compilazione di una libreria di importazione e di un file di esportazione.](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019)

## <a name="using-an-import-library"></a>Uso di una libreria di importazione

Ad esempio, per chiamare la [**funzione CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) è necessario collegare il codice alla libreria di importazione User32.lib. Il motivo è che **CreateWindow** si trova in una DLL di sistema denominata User32.dll e User32.lib è la libreria di importazione usata per risolvere le chiamate alle funzioni esportate in User32.dll nel codice. Il linker crea una tabella che contiene l'indirizzo di ogni chiamata di funzione. Le chiamate alle funzioni in una DLL verranno fisse quando la DLL viene caricata. Durante l'inizializzazione del processo, il sistema carica User32.dll perché dipende dalle funzioni esportate nella DLL e aggiorna le voci nella tabella degli indirizzi delle funzioni. Tutte le chiamate **a CreateWindow** richiamano la funzione esportata da User32.dll.

Per informazioni, vedere [Collegamento implicito a una DLL.](/previous-versions/d14wsce5(v=vs.140))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una libreria a collegamento dinamico semplice](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
