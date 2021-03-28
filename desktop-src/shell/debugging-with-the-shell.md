---
description: In questo argomento viene illustrato come eseguire il debug di dll di estensione dello spazio dei nomi e Shell
title: Debug con la shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525380"
---
# <a name="debugging-with-the-shell"></a>Debug con la shell

In questo argomento viene illustrato come eseguire il debug di dll di estensione dello spazio dei nomi e Shell

-   [Esecuzione della shell in un debugger](#running-the-shell-under-a-debugger)
-   [Esecuzione e test delle estensioni della shell](#running-and-testing-shell-extensions)
-   [Scaricamento della DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Esecuzione della shell in un debugger

Per eseguire il debug dell'estensione, è necessario eseguire la shell dal debugger. A tale scopo, seguire questa procedura:

1.  Caricare il progetto dell'estensione nel debugger, ma non eseguirlo.
2.  Arrestare la Shell.

    -   Per Windows Vista e versioni successive:
        1.  Visualizzare il menu **Start** .
        2.  Premere CTRL + MAIUSC e fare clic con il pulsante destro del mouse sullo sfondo della metà destra del menu **Start** .
        3.  Dal menu visualizzato scegliere **Esci da Esplora risorse**.
    -   Per Windows XP:
        1.  Dal menu **Start** scegliere **Arresta**.
        2.  Premere CTRL + ALT + MAIUSC e fare clic su **No** nella finestra di dialogo **arresta Windows** .

    La shell viene ora arrestata, ma tutte le altre applicazioni sono ancora in esecuzione, incluso il debugger.

3.  Impostare il debugger per eseguire la DLL di estensione con Explorer.exe dalla directory **Windows** .
4.  Eseguire il progetto dal debugger. La shell verrà avviata come di consueto, ma il debugger verrà collegato al processo della shell.

## <a name="running-and-testing-shell-extensions"></a>Esecuzione e test delle estensioni della shell

È possibile eseguire e testare le estensioni in un processo separato di Esplora risorse per evitare di arrestare e riavviare il desktop e la barra delle applicazioni. Il desktop e la barra delle applicazioni possono essere ancora usati durante l'esecuzione e il test delle estensioni.

Per abilitare questa funzionalità, aggiungere la seguente \_ voce reg DWORD al registro di sistema.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Per rendere effettive queste voci, è necessario disconnettersi e accedere di nuovo. Questa impostazione consente di creare le finestre del desktop e della barra delle applicazioni in un processo di Explorer.exe e tutte le altre finestre di esplorazione e cartella da aprire in un processo di Explorer.exe diverso.

Oltre a rendere più semplice l'esecuzione e il test delle estensioni, questa impostazione rende il desktop più affidabile in quanto si riferisce alle estensioni della shell. Molte estensioni di questo tipo (ad esempio, le estensioni del menu di scelta rapida) verranno caricate nel processo di Explorer.exe non desktop. Se questo processo termina, il desktop e la barra delle applicazioni non saranno interessati e la finestra Esplora o cartella successiva creerà nuovamente il processo terminato.

## <a name="unloading-the-dll"></a>Scaricamento della DLL

La shell Scarica automaticamente qualsiasi DLL quando il conteggio di utilizzo è pari a zero, ma solo dopo che la DLL non è stata utilizzata per un certo periodo di tempo. Questo periodo di tempo inattivo potrebbe essere inaccettabile a volte, soprattutto quando viene eseguito il debug di una DLL di estensione della shell. È possibile abbreviare il periodo di inattività aggiungendo le informazioni seguenti al registro di sistema.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



