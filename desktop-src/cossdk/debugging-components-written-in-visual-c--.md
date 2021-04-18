---
description: Quando si è pronti per eseguire il debug della funzionalità COM+ nei componenti di Microsoft Visual C++, è possibile configurare Visual C++ progetto o lo strumento di amministrazione Servizi componenti per avviare il debugger.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Debug di componenti scritti in Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304629"
---
# <a name="debugging-components-written-in-visual-c"></a>Debug di componenti scritti in Visual C++

Quando si è pronti per eseguire il debug della funzionalità COM+ nei componenti di Microsoft Visual C++, è possibile configurare Visual C++ progetto o lo strumento di amministrazione Servizi componenti per avviare il debugger. Se si utilizza Visual C++, è possibile eseguire il debug con un client remoto utilizzando la RPC OLE e il debug JIT (just-in-Time). Se non si riesce a eseguire il client nel debugger o se il client è in esecuzione in un altro computer, è possibile usare l'impostazione **di avvio com+ in debugger** . Lo strumento di amministrazione Servizi componenti è presente in come casella di controllo nella scheda **Avanzate** della finestra di dialogo **Proprietà** applicazione com+.

Al termine del debug, è necessario arrestare le applicazioni COM+ di cui si esegue il debug. Se un processo server viene lasciato in esecuzione, è possibile che venga generato un messaggio di errore al successivo tentativo di compilazione di una DLL quando la DLL esistente è ancora caricata in memoria. Per arrestare un'applicazione COM+, fare clic con il pulsante destro del mouse sull'applicazione nell'albero della console e quindi scegliere **Arresta**.

> [!Note]  
> Se si utilizzano le transazioni, potrebbe essere necessario aumentare anche il timeout della transazione, il cui valore predefinito è 60 secondi. È anche possibile specificare un valore pari a 0, specificando in modo efficace un periodo di timeout delle transazioni infinito. Utilizzando lo strumento di amministrazione Servizi componenti, modificare l'impostazione di timeout della transazione nella scheda **Opzioni** della finestra **Proprietà computer locale** .

 

## <a name="debugging-server-application-components-with-visual-c"></a>Debug dei componenti dell'applicazione server con Visual C++

Quando si esegue il debug di applicazioni server COM+, è possibile eseguire il debug delle chiamate remote caricando il client e l'applicazione server nel debugger. Con Visual C++, è possibile eseguire il debug delle chiamate remote ai componenti tramite le impostazioni JIT (just-in-Time) e OLE RPC. L'impostazione JIT induce il componente compilato ad avviare il debugger Visual C++ quando si verifica un errore. l'impostazione OLE RPC consente al debugger di eseguire il passaggio da client a componente mentre si esegue il codice un'istruzione alla volta.

Quando queste funzionalità sono abilitate, è possibile avviare il client nel debugger. Quando il client effettua una chiamata al componente, il debugger eseguirà l'istruzione nel codice del componente nel processo server, anche se il server si trova in un computer diverso nella rete. Una sessione di debug viene avviata automaticamente nel computer server, se necessario. Analogamente, il passaggio successivo dell'istruzione return nel codice del componente restituirà il debug all'istruzione successiva nel codice del client.

> [!Note]  
> È possibile salvare alcuni passaggi utilizzando l'impostazione di **avvio com+ in debugger** . In questo modo è possibile specificare il debugger Visual C++ (o un altro) senza dover effettuare particolari impostazioni di debug nell'ambiente Visual C++. Lo strumento di amministrazione Servizi componenti è presente in come casella di controllo nella scheda **Avanzate** della finestra di dialogo **Proprietà** applicazione com+. Per ulteriori informazioni, vedere "debug senza Visual C++" in questo argomento.

 

Quando l'applicazione COM+ che contiene il componente è un'applicazione server, è necessario innanzitutto arrestare l'applicazione utilizzando lo strumento di amministrazione Servizi componenti. A tale scopo, fare clic con il pulsante destro del mouse sull'applicazione COM+ nell'albero della console e quindi scegliere **Arresta**.

**Per abilitare il debug RPC in Visual C++**

1.  In Visual C++ scegliere **Opzioni** dal menu **strumenti** .

2.  Nella scheda **debug** della finestra di dialogo **Opzioni** selezionare le caselle di controllo debug **RPC OLE** e **debug JIT** .

3.  Fare clic su **OK**.

Per iniziare il debug, avviare il progetto client nel debugger.

È anche possibile eseguire il debug del componente senza avviare il client nel debugger. In questo caso, il componente deve avviare il debugger autonomamente. Per eseguire questa operazione, è necessario che il progetto componente specifichi un eseguibile per la sessione di debug, insieme all'ID applicazione COM+.

**Per abilitare un componente dell'applicazione server per avviare il debugger Visual C++**

1.  Scegliere **Impostazioni** dal menu **progetto** .

2.  Nella finestra di dialogo **Impostazioni progetto** , nella casella **impostazioni per** Selezionare **debug Win32**.

3.  Nella scheda **debug** della casella **categoria** Selezionare **generale**.

4.  Nella casella **eseguibile per la sessione di debug** immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID applicazione dell'applicazione com+ contenente il componente.

    > [!Note]  
    > Utilizzando lo strumento di amministrazione Servizi componenti, sarà possibile trovare l'ID applicazione nella scheda **generale** della finestra di dialogo **Proprietà** dell'applicazione com+. Di seguito è illustrato un esempio:

     

    > [!Note]  
    > C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: {applicationID}

     

5.  Fare clic su **OK**.

È ora possibile impostare punti di interruzione, avviare il debugger e iniziare a eseguire chiamate al componente.

## <a name="debugging-library-application-components-with-visual-c"></a>Debug dei componenti dell'applicazione libreria con Visual C++

Per eseguire il debug dei componenti in un'applicazione di libreria, è necessario configurare il progetto del client perché il processo del client ospiterà l'applicazione della libreria.

**Per abilitare il debug dell'applicazione libreria con Visual C++**

1.  In Visual C++ scegliere **Impostazioni** dal menu **progetto** .

2.  Nella finestra di dialogo **Impostazioni progetto** , nella casella **impostazioni per** , fare clic su **debug Win32**.

3.  Nella scheda **debug** della casella **categoria** fare clic su **DLL aggiuntive**.

4.  Nell'elenco **moduli** aggiungere le dll del componente nell'applicazione libreria. In questo modo è possibile impostare punti di interruzione prima che la DLL venga effettivamente caricata.

5.  Fare clic su **OK**.

## <a name="debugging-without-visual-c"></a>Debug senza Visual C++

Indipendentemente dall'utilizzo Visual C++ per il debug, è possibile utilizzare l'impostazione **avvia in debugger** per specificare il debugger in cui devono essere eseguiti i componenti.

**Per specificare un debugger dallo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console selezionare l'applicazione libreria COM+ contenente i componenti di cui si desidera eseguire il debug.

2.  Fare clic con il pulsante destro del mouse sull'applicazione, quindi scegliere **Proprietà**.

3.  Nella finestra di dialogo **Proprietà** dell'applicazione fare clic sulla scheda **Avanzate** .

4.  In **debug** selezionare la casella **di controllo avvia nel debugger** .

5.  Nella casella **percorso debugger** immettere il percorso del debugger che si desidera utilizzare. È anche possibile fare clic su **Sfoglia** per individuare il debugger. Di seguito è riportato un esempio: C: \\ WinNT \\ system32 \\Ntsd.exe.

6.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di componenti scritti in Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



