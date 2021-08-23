---
title: Installazione e registrazione di gestori di protocollo (funzionalità dell Windows legacy)
description: L'installazione dei gestori di protocollo comporta la copia delle DLL in un percorso appropriato nella directory Programmi e la loro registrazione.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716561"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Installazione e registrazione di gestori di protocollo (funzionalità dell Windows legacy)

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

**L'installazione dei gestori di** protocollo comporta la copia delle DLL in un percorso appropriato nella directory Programmi e la loro registrazione.

Questa sezione contiene i seguenti argomenti:

-   [Linee guida per l'installazione](#installation-guidelines)
-   [Per registrare i gestori di protocollo](#to-register-protocol-handlers)
-   [Per registrare le estensioni della shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Linee guida per l'installazione

I gestori di protocollo devono implementare la registrazione automatica per l'installazione e devono seguire queste linee guida:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È **necessario creare una voce** Installazione applicazioni per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del Registro di sistema per il particolare tipo di file o archivio che il componente aggiuntivo corrente è in conoscenza.
-   Se viene sovrascritto un componente aggiuntivo precedente, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e renderlo nuovamente il componente aggiuntivo predefinito per quel tipo di file.

## <a name="to-register-protocol-handlers"></a>Per registrare i gestori di protocollo

È necessario creare sedicenti voci nel Registro di sistema per registrare il componente gestore di protocollo, dove:

-   *Ver \_ Ind \_ ProgID è il ProgID* indipendente dalla versione dell'implementazione del gestore di protocollo
-   *Ver \_ Dep \_ ProgID è il ProgID* dipendente dalla versione dell'implementazione del gestore di protocollo
-   *CLSID \_ 1 è* il CLSID dell'implementazione del gestore di protocollo

1.  Registrare il ProgID indipendente dalla versione con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  Registrare il ProgID dipendente dalla versione con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Registrare il CLSID del gestore di protocollo con le chiavi e i valori seguenti:

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  Registrare il gestore di protocollo Windows Desktop Search:

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>Per registrare le estensioni della shell

È necessario creare due voci nel Registro di sistema per registrare l'estensione shell del gestore di protocollo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




