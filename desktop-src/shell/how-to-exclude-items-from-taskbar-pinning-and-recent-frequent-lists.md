---
description: Le applicazioni, i processi e le finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco dei menu Start (MFU) usato più di frequente.
title: Come escludere elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979562"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="d749a-103">Come escludere elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti</span><span class="sxs-lookup"><span data-stu-id="d749a-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="d749a-104">Le applicazioni, i processi e le finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco dei menu **Start** (MFU) usato più di frequente.</span><span class="sxs-lookup"><span data-stu-id="d749a-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="d749a-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="d749a-105">Instructions</span></span>


<span data-ttu-id="d749a-106">Esistono tre meccanismi per eseguire l'esclusione di elementi dal blocco della barra delle applicazioni e dagli elenchi recenti/frequenti:</span><span class="sxs-lookup"><span data-stu-id="d749a-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="d749a-107">Aggiungere la voce NoStartPage alla registrazione dell'applicazione, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d749a-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="d749a-108">I dati associati alla voce NoStartPage vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d749a-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="d749a-109">È necessaria solo la presenza della voce.</span><span class="sxs-lookup"><span data-stu-id="d749a-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="d749a-110">Pertanto, il tipo ideale per NoStartPage è **reg \_ None**.</span><span class="sxs-lookup"><span data-stu-id="d749a-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="d749a-111">Si noti che qualsiasi utilizzo di un ID modello utente applicazione esplicito (AppUserModelID) sostituisce la voce NoStartPage.</span><span class="sxs-lookup"><span data-stu-id="d749a-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="d749a-112">Se un AppUserModelID esplicito viene applicato a un collegamento, a un processo o a una finestra, diventa aggiungibili e idoneo per l'elenco MFU del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="d749a-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="d749a-113">Impostare la proprietà [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) in Windows e i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="d749a-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="d749a-114">Questa proprietà deve essere impostata su una finestra prima che venga impostata la proprietà [ \_ \_ ID AppUserModel pkey](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="d749a-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="d749a-115">Aggiungere un AppUserModelID esplicito come valore nella seguente sottochiave del registro di sistema, come illustrato in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="d749a-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="d749a-116">Ogni voce è un valore **reg \_ null** con il nome del AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="d749a-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="d749a-117">Qualsiasi AppUserModelID trovato in questo elenco non è aggiungibili e non è idoneo per l'inclusione nell'elenco MFU del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="d749a-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="d749a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d749a-118">Remarks</span></span>

<span data-ttu-id="d749a-119">Tenere presente che alcuni file eseguibili, oltre a collegamenti che contengono determinate stringhe nei rispettivi nomi, vengono automaticamente esclusi dal blocco e dall'inclusione nell'elenco MFU.</span><span class="sxs-lookup"><span data-stu-id="d749a-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="d749a-120">Questa esclusione automatica può essere sottoposta a override applicando un AppUserModelID esplicito.</span><span class="sxs-lookup"><span data-stu-id="d749a-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="d749a-121">Se una delle stringhe seguenti, indipendentemente dalla distinzione tra maiuscole e minuscole, è inclusa nel nome del collegamento, il programma non è aggiungibili e non viene visualizzato nell'elenco degli elementi utilizzati più di frequente (non applicabile a Windows 10):</span><span class="sxs-lookup"><span data-stu-id="d749a-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="d749a-122">Documentazione</span><span class="sxs-lookup"><span data-stu-id="d749a-122">Documentation</span></span>
-   <span data-ttu-id="d749a-123">Help</span><span class="sxs-lookup"><span data-stu-id="d749a-123">Help</span></span>
-   <span data-ttu-id="d749a-124">Installazione</span><span class="sxs-lookup"><span data-stu-id="d749a-124">Install</span></span>
-   <span data-ttu-id="d749a-125">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="d749a-125">More Info</span></span>
-   <span data-ttu-id="d749a-126">Leggi</span><span class="sxs-lookup"><span data-stu-id="d749a-126">Read me</span></span>
-   <span data-ttu-id="d749a-127">Leggi prima</span><span class="sxs-lookup"><span data-stu-id="d749a-127">Read First</span></span>
-   <span data-ttu-id="d749a-128">File Leggimi</span><span class="sxs-lookup"><span data-stu-id="d749a-128">Readme</span></span>
-   <span data-ttu-id="d749a-129">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="d749a-129">Remove</span></span>
-   <span data-ttu-id="d749a-130">Configurazione</span><span class="sxs-lookup"><span data-stu-id="d749a-130">Setup</span></span>
-   <span data-ttu-id="d749a-131">Supporto</span><span class="sxs-lookup"><span data-stu-id="d749a-131">Support</span></span>
-   <span data-ttu-id="d749a-132">Novità</span><span class="sxs-lookup"><span data-stu-id="d749a-132">What's New</span></span>

<span data-ttu-id="d749a-133">L'elenco di programmi seguente non è aggiungibili e viene escluso dall'elenco degli elementi utilizzati più di frequente:</span><span class="sxs-lookup"><span data-stu-id="d749a-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="d749a-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-134">Applaunch.exe</span></span>
-   <span data-ttu-id="d749a-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-135">Control.exe</span></span>
-   <span data-ttu-id="d749a-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="d749a-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-137">Dllhost.exe</span></span>
-   <span data-ttu-id="d749a-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="d749a-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-139">Hh.exe</span></span>
-   <span data-ttu-id="d749a-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-140">Install.exe</span></span>
-   <span data-ttu-id="d749a-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-141">Isuninst.exe</span></span>
-   <span data-ttu-id="d749a-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="d749a-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-143">Mmc.exe</span></span>
-   <span data-ttu-id="d749a-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-144">Mshta.exe</span></span>
-   <span data-ttu-id="d749a-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-145">Msiexec.exe</span></span>
-   <span data-ttu-id="d749a-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-146">Msoobe.exe</span></span>
-   <span data-ttu-id="d749a-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-147">Rundll32.exe</span></span>
-   <span data-ttu-id="d749a-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-148">Setup.exe</span></span>
-   <span data-ttu-id="d749a-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-149">St5unst.exe</span></span>
-   <span data-ttu-id="d749a-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-150">Unwise.exe</span></span>
-   <span data-ttu-id="d749a-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-151">Unwise32.exe</span></span>
-   <span data-ttu-id="d749a-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-152">Werfault.exe</span></span>
-   <span data-ttu-id="d749a-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="d749a-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="d749a-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="d749a-155">Wuapp.exe</span></span>

<span data-ttu-id="d749a-156">Gli elenchi precedenti vengono archiviati nei seguenti valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d749a-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="d749a-157">Questi elenchi non devono essere modificati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d749a-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="d749a-158">Per la stessa esperienza, utilizzare uno dei metodi dell'elenco di esclusioni descritti in precedenza in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d749a-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="d749a-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d749a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d749a-160">Barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="d749a-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="d749a-161">Estensioni della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="d749a-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
