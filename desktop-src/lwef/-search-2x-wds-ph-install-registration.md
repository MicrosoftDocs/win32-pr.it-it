---
title: Installazione e registrazione di gestori di protocollo (funzionalità legacy dell'ambiente Windows)
description: L'installazione dei gestori di protocollo comporta la copia delle DLL in una posizione appropriata nella directory programmi e la relativa registrazione.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340263"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>Installazione e registrazione di gestori di protocollo (funzionalità legacy dell'ambiente Windows)

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

L'installazione dei **gestori di protocollo** comporta la copia delle dll in una posizione appropriata nella directory programmi e la relativa registrazione.

Questa sezione contiene i seguenti argomenti:

-   [Linee guida per l'installazione](#installation-guidelines)
-   [Per registrare i gestori di protocollo](#to-register-protocol-handlers)
-   [Per registrare le estensioni della shell](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Linee guida per l'installazione

I gestori di protocollo devono implementare la registrazione automatica per l'installazione e attenersi alle linee guida seguenti:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.
-   Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e impostarlo di nuovo come componente aggiuntivo predefinito per quel tipo di file.

## <a name="to-register-protocol-handlers"></a>Per registrare i gestori di protocollo

È necessario creare quattordici voci nel registro di sistema per registrare il componente gestore di protocollo, dove:

-   *Ver \_ IND \_ ProgID* è il ProgID indipendente dalla versione dell'implementazione del gestore di protocollo
-   *Ver \_ DEP \_ ProgID* è il ProgID dipendente dalla versione dell'implementazione del gestore di protocollo
-   *CLSID \_ 1* è il CLSID dell'implementazione del gestore di protocollo

1.  Registrare la versione Independent ProgID con le chiavi e i valori seguenti:

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

4.  Registrare il gestore di protocollo con Windows Desktop Search:

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

È necessario creare due voci nel registro di sistema per registrare l'estensione della shell del gestore del protocollo.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




