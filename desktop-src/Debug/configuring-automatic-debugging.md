---
description: Gli utenti possono configurare il debug automatico per consentire loro di determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurazione del debug automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125748"
---
# <a name="configuring-automatic-debugging"></a>Configurazione del debug automatico

Gli utenti possono configurare il debug automatico per consentire loro di determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.

## <a name="configuring-automatic-debugging-for-system-crashes"></a>Configurazione del debug automatico per arresti anomali del sistema

Per configurare il computer di destinazione in modo da generare un file di dump di arresto anomalo del sistema quando il sistema smette di rispondere, usare l'applicazione di **sistema** nel pannello di controllo Fare clic su **impostazioni di sistema avanzate**, che consente di visualizzare la finestra di dialogo **proprietà del sistema** . Nella scheda **Avanzate** della casella fare clic su **Impostazioni** in **avvio e ripristino**, quindi utilizzare le opzioni di ripristino appropriate. In alternativa, è possibile configurare le opzioni di dump di arresto anomalo del sistema utilizzando la seguente chiave del registro

**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **CrashControl**

Il file che è possibile specificare è il file di dump di arresto anomalo del sistema. Il nome predefinito è Memory. dmp. È possibile eseguire il debug di un dump di arresto anomalo del sistema con un debugger in modalità kernel, ad esempio WinDbg o KD. Per ulteriori informazioni, vedere la documentazione inclusa nel debugger.

## <a name="configuring-automatic-debugging-for-application-crashes"></a>Configurazione del debug automatico per arresti anomali dell'applicazione

Quando un'applicazione smette di rispondere, ad esempio dopo una violazione di accesso, il sistema richiama automaticamente un debugger specificato nel registro di sistema per il debug di post-mortem, l'ID del processo e l'handle di evento vengono passati al debugger se la riga di comando è configurata correttamente. Nella procedura riportata di seguito viene descritto come specificare un debugger nel registro di sistema.

**Per impostare un debugger come debugger di post-mortem**

1.  Passare alla chiave del registro di sistema seguente:

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Aggiungere o modificare il valore del **debugger** utilizzando una \_ stringa reg SZ che specifica la riga di comando per il debugger.

    La stringa deve includere il percorso completo dell'eseguibile del debugger. Indica l'ID processo e l'handle evento con i parametri "% LD" alla riga di comando del debugger. Debugger diversi possono disporre di proprie sintassi dei parametri per indicare questi valori. Quando viene richiamato il debugger, il primo "% LD" viene sostituito con l'ID del processo e la seconda "% LD" viene sostituita con l'handle dell'evento.

    Il testo seguente è un esempio di come configurare WinDbg come debugger.

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  Se si desidera che il debugger venga richiamato senza interazione dell'utente, aggiungere o modificare il valore **auto** utilizzando una \_ stringa reg SZ che specifica se il sistema deve visualizzare una finestra di dialogo per l'utente prima che venga richiamato il debugger. La stringa "1" Disabilita la finestra di dialogo; la stringa "0" Abilita la finestra di dialogo.

## <a name="excluding-an-application-from-automatic-debugging"></a>Esclusione di un'applicazione dal debug automatico

Nella procedura seguente viene descritto come escludere un'applicazione dal debug automatico dopo che il valore **auto** sotto la chiave **AeDebug** è stato impostato su 1.

**Per escludere un'applicazione dal debug automatico**

1.  Passare alla chiave del registro di sistema seguente:

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**

2.  Aggiungere un \_ valore reg DWORD alla sottochiave **autoesclusione** , dove il nome è il nome del file eseguibile e il valore è 1. Per impostazione predefinita, il Gestione finestre desktop (Dwm.exe) viene escluso dal debug automatico. in caso contrario, può verificarsi un deadlock del sistema se Dwm.exe smette di rispondere (l'utente non può visualizzare l'interfaccia visualizzata dal debugger perché Dwm.exe non risponde e Dwm.exe non può terminare perché è mantenuta dal debugger).

    **Windows Server 2003 e Windows XP:** La sottochiave **autoesclusione** non è disponibile. non è quindi possibile escludere alcuna applicazione, incluso Dwm.exe, dal debug automatico.

Le voci del registro di sistema **AeDebug** predefinite possono essere rappresentate come segue:

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

[Abilitazione del debug postmortem con WinDbg](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
