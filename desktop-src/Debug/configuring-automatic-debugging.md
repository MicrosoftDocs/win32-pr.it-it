---
description: Gli utenti possono configurare il debug automatico per determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurazione del debug automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990f2f52e6227e4b1a2cf92656794c90fb5d465915a5d888025d0f3b2c438630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076505"
---
# <a name="configuring-automatic-debugging"></a>Configurazione del debug automatico

Gli utenti possono configurare il debug automatico per determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configurazione del debug automatico per arresti anomali del sistema

Per configurare il computer di destinazione in modo da generare un file di dump di arresto anomalo del sistema quando il sistema smette di rispondere, usare **l'applicazione System** Pannello di controllo. Fare **clic su Impostazioni di sistema avanzate**, che visualizza la finestra di dialogo **Proprietà** sistema . Nella scheda **Avanzate** di tale casella fare clic su Impostazioni **in** Avvio e ripristino **e** quindi usare le opzioni di ripristino appropriate. In alternativa, è possibile configurare le opzioni di dump di arresto anomalo del sistema usando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

Il file che è possibile specificare è il file di dump dell'arresto anomalo del sistema. Il nome predefinito è Memory.dmp. È possibile eseguire il debug di un dump di arresto anomalo del sistema con un debugger in modalità kernel, ad esempio WinDbg o KD. Per altre informazioni, vedere la documentazione inclusa nel debugger.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configurazione del debug automatico per arresti anomali dell'applicazione

Quando un'applicazione smette di rispondere (ad esempio, dopo una violazione di accesso), il sistema richiama automaticamente un debugger specificato nel Registro di sistema per il debug post-mortem, l'ID processo e l'handle di evento vengono passati al debugger se la riga di comando è configurata correttamente. La procedura seguente descrive come specificare un debugger nel Registro di sistema.

**Per impostare un debugger come debugger post-mortem**

1.  Passare alla chiave del Registro di sistema seguente:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Aggiungere o modificare il **valore Debugger** usando una stringa \_ REG SZ che specifica la riga di comando per il debugger.

    La stringa deve includere il percorso completo dell'eseguibile del debugger. Indicare l'ID processo e l'handle di evento con i parametri "%ld" alla riga di comando del debugger. Debugger diversi possono avere sintassi di parametri proprie per indicare questi valori. Quando viene richiamato il debugger, il primo "%ld" viene sostituito con l'ID processo e il secondo "%ld" viene sostituito con l'handle dell'evento.

    Il testo seguente è un esempio di come configurare WinDbg come debugger.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Se si vuole che il debugger venga richiamato  senza interazione dell'utente, aggiungere o modificare il valore Auto usando una stringa REG SZ che specifica se il sistema deve visualizzare una finestra di dialogo all'utente prima che venga richiamato \_ il debugger. La stringa "1" disabilita la finestra di dialogo. la stringa "0" abilita la finestra di dialogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Esclusione di un'applicazione dal debug automatico

La procedura seguente descrive come escludere un'applicazione dal debug automatico dopo che il valore **Auto** nella chiave **AeDebug** è stato impostato su 1.

**Per escludere un'applicazione dal debug automatico**

1.  Passare alla chiave del Registro di sistema seguente:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Aggiungere un valore DWORD REG alla \_ **sottochiave AutoExclusionList,** dove il nome è il nome del file eseguibile e il valore è 1. Per impostazione predefinita, il Gestione finestre desktop (Dwm.exe) è escluso dal debug automatico perché in caso contrario, un deadlock di sistema può verificarsi se Dwm.exe smette di rispondere (l'utente non può visualizzare l'interfaccia visualizzata dal debugger perché Dwm.exe non risponde e Dwm.exe non può terminare perché è mantenuto dal debugger).

    **Windows Server 2003 e Windows XP:** La **sottochiave AutoExclusionList** non è disponibile. pertanto non è possibile escludere alcuna applicazione, incluso Dwm.exe, dal debug automatico.

Le voci predefinite del Registro di sistema **AeDebug** possono essere rappresentate come segue:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione del debug post-debug con WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
