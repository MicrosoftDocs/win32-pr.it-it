---
description: Quando si descrive il debug, vengono usati i termini seguenti.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologia relativa al debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb8de5035887f3d3c19cca1e8475ff17cb930b1142c712481e096e0e612ea81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692071"
---
# <a name="debugging-terminology"></a>Terminologia relativa al debug

Quando si descrive il debug, vengono usati i termini seguenti.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Schermata blu
</dt> <dd>

Quando il sistema rileva un problema hardware, un'incoerenza dei dati o un errore simile, può essere visualizzata una schermata blu contenente informazioni che possono essere usate per determinare la causa dell'errore. Queste informazioni includono il codice STOP e indica se è stato creato un file di dump di arresto anomalo del sistema. Può anche includere un elenco di driver caricati e un'analisi dello stack.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>File di dump di arresto anomalo del sistema
</dt> <dd>

È possibile configurare il sistema per scrivere informazioni in un file di dump di arresto anomalo del sistema sul disco rigido ogni volta che viene generato un codice STOP. Il file contiene informazioni che il debugger può usare per analizzare l'errore. Questo file può essere grande quanto la memoria fisica contenuta nel computer.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger
</dt> <dd>

Programma progettato per rilevare, individuare e correggere gli errori in un altro programma. Consente allo sviluppatore di eseguire il processo e i relativi thread, monitorando la memoria, le variabili e altri elementi del contesto del processo e del thread.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modalità kernel
</dt> <dd>

Modalità del processore in cui vengono eseguiti i servizi di sistema e i driver di dispositivo. Tutte le interfacce e le istruzioni della CPU sono disponibili e tutta la memoria è accessibile.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>File minidump
</dt> <dd>

Le applicazioni possono produrre file di minidump in modalità utente, che contengono un utile subset delle informazioni contenute in un file di dump di arresto anomalo del sistema. Per altre informazioni, vedere [Minidump Files](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Codice STOP
</dt> <dd>

Codice di errore che identifica l'errore che ha impedito al kernel di sistema di continuare l'esecuzione.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>File di simboli
</dt> <dd>

Tutte le applicazioni di sistema, i driver e le DLL vengono compilati in modo che le informazioni di debug risiedano in file separati noti come file di simboli. Di conseguenza, il sistema è più piccolo e più veloce, ma è comunque possibile eseguirne il debug se i file di simboli sono installati. Per altre informazioni, vedere [File di simboli.](symbol-files.md)

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modalità utente
</dt> <dd>

Modalità del processore in cui vengono eseguite le applicazioni. In questa modalità è disponibile un set limitato di interfacce e l'accesso ai dati di sistema è limitato.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del debug automatico](configuring-automatic-debugging.md)
</dt> </dl>

 

 



