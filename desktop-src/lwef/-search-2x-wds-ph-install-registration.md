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
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="12a58-103">Installazione e registrazione di gestori di protocollo (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="12a58-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="12a58-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="12a58-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="12a58-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="12a58-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="12a58-106">L'installazione dei **gestori di protocollo** comporta la copia delle dll in una posizione appropriata nella directory programmi e la relativa registrazione.</span><span class="sxs-lookup"><span data-stu-id="12a58-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="12a58-107">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="12a58-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="12a58-108">Linee guida per l'installazione</span><span class="sxs-lookup"><span data-stu-id="12a58-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="12a58-109">Per registrare i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="12a58-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="12a58-110">Per registrare le estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="12a58-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="12a58-111">Linee guida per l'installazione</span><span class="sxs-lookup"><span data-stu-id="12a58-111">Installation Guidelines</span></span>

<span data-ttu-id="12a58-112">I gestori di protocollo devono implementare la registrazione automatica per l'installazione e attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a58-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="12a58-113">Il programma di installazione deve usare il programma di installazione EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="12a58-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="12a58-114">È necessario fornire le note sulla versione.</span><span class="sxs-lookup"><span data-stu-id="12a58-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="12a58-115">È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.</span><span class="sxs-lookup"><span data-stu-id="12a58-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="12a58-116">Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.</span><span class="sxs-lookup"><span data-stu-id="12a58-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="12a58-117">Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="12a58-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="12a58-118">Se un componente aggiuntivo più recente ha sovrascritto il componente aggiuntivo precedente, dovrebbe essere possibile ripristinare la funzionalità del componente aggiuntivo precedente e impostarlo di nuovo come componente aggiuntivo predefinito per quel tipo di file.</span><span class="sxs-lookup"><span data-stu-id="12a58-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="12a58-119">Per registrare i gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="12a58-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="12a58-120">È necessario creare quattordici voci nel registro di sistema per registrare il componente gestore di protocollo, dove:</span><span class="sxs-lookup"><span data-stu-id="12a58-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="12a58-121">*Ver \_ IND \_ ProgID* è il ProgID indipendente dalla versione dell'implementazione del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="12a58-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="12a58-122">*Ver \_ DEP \_ ProgID* è il ProgID dipendente dalla versione dell'implementazione del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="12a58-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="12a58-123">*CLSID \_ 1* è il CLSID dell'implementazione del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="12a58-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="12a58-124">Registrare la versione Independent ProgID con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a58-124">Register the version independent ProgID with the following keys and values:</span></span>

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

2.  <span data-ttu-id="12a58-125">Registrare il ProgID dipendente dalla versione con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a58-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="12a58-126">Registrare il CLSID del gestore di protocollo con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a58-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

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

4.  <span data-ttu-id="12a58-127">Registrare il gestore di protocollo con Windows Desktop Search:</span><span class="sxs-lookup"><span data-stu-id="12a58-127">Register the protocol handler with Windows Desktop Search:</span></span>

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

## <a name="to-register-shell-extensions"></a><span data-ttu-id="12a58-128">Per registrare le estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="12a58-128">To Register Shell Extensions</span></span>

<span data-ttu-id="12a58-129">È necessario creare due voci nel registro di sistema per registrare l'estensione della shell del gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="12a58-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




