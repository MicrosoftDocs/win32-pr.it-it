---
description: Questo argomento illustra come eseguire il debug delle DLL di estensione della shell e dello spazio dei nomi.
title: Debug con la shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 276023e5628ab7390398fd7bd367be32e45c13825fcf96625104be1ded8735de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032829"
---
# <a name="debugging-with-the-shell"></a>Debug con la shell

Questo argomento illustra come eseguire il debug delle DLL di estensione della shell e dello spazio dei nomi.

-   [Esecuzione della shell in un debugger](#running-the-shell-under-a-debugger)
-   [Esecuzione e test delle estensioni della shell](#running-and-testing-shell-extensions)
-   [Scaricamento della DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>Esecuzione della shell in un debugger

Per eseguire il debug dell'estensione, è necessario eseguire la shell dal debugger. Seguire questa procedura:

1.  Caricare il progetto dell'estensione nel debugger, ma non eseguirlo.
2.  Arrestare la shell.

    -   Per Windows Vista e versioni successive:
        1.  Visualizzare il menu **Start.**
        2.  Premere CTRL+MAIUSC e fare clic con il pulsante destro del mouse sullo sfondo della metà destra del menu **Start.**
        3.  Scegliere Esci da Esplora risorse dal menu **visualizzato.**
    -   Per Windows XP:
        1.  Dal menu **Start** scegliere **Arresta**.
        2.  Premere CTRL+ALT+MAIUSC e fare clic **su No** nella finestra di **dialogo Windows** arresta.

    La shell è ora arrestata, ma tutte le altre applicazioni sono ancora in esecuzione, incluso il debugger.

3.  Impostare il debugger per eseguire la DLL di estensione Explorer.exe dalla directory **Windows.**
4.  Eseguire il progetto dal debugger. La shell verrà avviata come di consueto, ma il debugger verrà collegato al processo della shell.

## <a name="running-and-testing-shell-extensions"></a>Esecuzione e test delle estensioni della shell

È possibile eseguire e testare le estensioni in un processo Windows Explorer separato per evitare di arrestare e riavviare il desktop e la barra delle applicazioni. Il desktop e la barra delle applicazioni possono comunque essere usati durante l'esecuzione e il test delle estensioni.

Per abilitare questa funzionalità, aggiungere la voce DWORD REG \_ seguente al Registro di sistema.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

Perché questa voce sia effettiva, è necessario disconnettersi e accedere di nuovo. Questa impostazione fa sì che le finestre del desktop e della barra delle applicazioni siano create in un processo di Explorer.exe e tutte le altre finestre di Esplora risorse e cartelle siano aperte in un processo Explorer.exe diverso.

Oltre a rendere più pratico l'esecuzione e il test delle estensioni, questa impostazione rende il desktop più affidabile in relazione alle estensioni della shell. Molte estensioni di questo tipo (ad esempio, le estensioni del menu di scelta rapida) verranno caricate nel processo Explorer.exe non desktop. Se questo processo termina, il desktop e la barra delle applicazioni non saranno interessati e la successiva finestra di esplorazione o cartella creerà di nuovo il processo terminato.

## <a name="unloading-the-dll"></a>Scaricamento della DLL

La shell scarica automaticamente qualsiasi DLL quando il numero di utilizzi è pari a zero, ma solo dopo che la DLL non è stata usata per un periodo di tempo. Questo periodo di inattività potrebbe essere inaccettabile a volte, soprattutto quando è in corso il debug di una DLL di estensione della shell. È possibile abbreviare il periodo di inattività aggiungendo le informazioni seguenti al Registro di sistema.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



