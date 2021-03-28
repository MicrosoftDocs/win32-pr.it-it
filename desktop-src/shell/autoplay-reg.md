---
description: In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'avvio automatico.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Abilitazione e disabilitazione dell'esecuzione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401626"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="a2405-103">Abilitazione e disabilitazione dell'esecuzione automatica</span><span class="sxs-lookup"><span data-stu-id="a2405-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="a2405-104">In molte situazioni potrebbe essere necessario disabilitare temporaneamente o in modo permanente l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="a2405-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="a2405-105">Ad esempio, l'esecuzione automatica potrebbe interferire con il funzionamento di un'applicazione in esecuzione e deve essere disabilitata per la durata.</span><span class="sxs-lookup"><span data-stu-id="a2405-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="a2405-106">Il sistema offre diversi modi per disabilitare l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="a2405-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="a2405-107">Eliminazione automatica a livello di codice</span><span class="sxs-lookup"><span data-stu-id="a2405-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="a2405-108">Uso del registro di sistema per disabilitare l'esecuzione automatica</span><span class="sxs-lookup"><span data-stu-id="a2405-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="a2405-109">AutoRun per altri tipi di supporti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a2405-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="a2405-110">Eliminazione automatica a livello di codice</span><span class="sxs-lookup"><span data-stu-id="a2405-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="a2405-111">Esistono diverse situazioni in cui potrebbe essere necessario disattivare l'esecuzione automatica a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="a2405-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="a2405-112">Di seguito sono riportati due esempi:</span><span class="sxs-lookup"><span data-stu-id="a2405-112">Two examples are:</span></span>

-   <span data-ttu-id="a2405-113">L'applicazione dispone di un programma di installazione che richiede all'utente di inserire un altro disco che potrebbe contenere un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="a2405-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="a2405-114">Durante il funzionamento dell'applicazione, l'utente potrebbe dover inserire un altro disco che potrebbe contenere un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="a2405-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="a2405-115">In entrambi i casi, in genere non si vuole avviare un'altra applicazione mentre è in corso l'originale.</span><span class="sxs-lookup"><span data-stu-id="a2405-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="a2405-116">Gli utenti possono disattivare manualmente l'esecuzione automatica tenendo premuto il tasto MAIUSC quando si inserisce il CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="a2405-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="a2405-117">Tuttavia, in genere è preferibile gestire questa operazione a livello di codice anziché a seconda dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a2405-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="a2405-118">Con i sistemi con shell [versione 4,70](versions.md) e successive, Windows invia un messaggio "QueryCancelAutoPlay" alla finestra in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a2405-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="a2405-119">L'applicazione può rispondere a questo messaggio per disattivare l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="a2405-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="a2405-120">Questo approccio viene usato dalle utilità di sistema, ad esempio la finestra di dialogo [Apri](../dlgbox/open-and-save-as-dialog-boxes.md) comune, per disabilitare l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="a2405-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="a2405-121">Nei frammenti di codice seguenti viene illustrato come impostare e gestire questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a2405-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="a2405-122">L'applicazione deve essere in esecuzione nella finestra in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a2405-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="a2405-123">Per prima cosa, registrare "QueryCancelAutoPlay" come messaggio di Windows:</span><span class="sxs-lookup"><span data-stu-id="a2405-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="a2405-124">Per ricevere questo messaggio, la finestra dell'applicazione deve essere in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a2405-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="a2405-125">Il gestore di messaggi deve restituire **true** per annullare Autorun e **false** per abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="a2405-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="a2405-126">Il frammento di codice seguente illustra come usare questo messaggio per disabilitare l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="a2405-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="a2405-127">Se l'applicazione usa una finestra di dialogo e deve rispondere a un messaggio "QueryCancelAutoPlay", non può semplicemente restituire **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="a2405-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="a2405-128">Chiamare invece [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) con *NIndex* impostato su **DWL \_ MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a2405-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="a2405-129">Impostare il parametro *dwNewLong* su **true** per annullare Autorun e **false** per abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="a2405-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="a2405-130">Ad esempio, la routine della finestra di dialogo di esempio seguente annulla l'esecuzione automatica quando riceve un messaggio "QueryCancelAutoPlay".</span><span class="sxs-lookup"><span data-stu-id="a2405-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="a2405-131">Uso del registro di sistema per disabilitare l'esecuzione automatica</span><span class="sxs-lookup"><span data-stu-id="a2405-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="a2405-132">Sono disponibili due valori del registro di sistema che possono essere usati per disabilitare in modo permanente AutoRun: NoDriveAutoRun e NoDriveTypeAutoRun.</span><span class="sxs-lookup"><span data-stu-id="a2405-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="a2405-133">Il primo valore Disabilita l'esecuzione automatica per le lettere di unità specificate e la seconda disabilita l'esecuzione automatica per una classe di unità.</span><span class="sxs-lookup"><span data-stu-id="a2405-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="a2405-134">Se uno di questi valori è impostato su Disabilita AutoRun per un particolare dispositivo, sarà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a2405-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="a2405-135">Per ulteriori informazioni sulla disabilitazione della funzionalità di AutoRun, vedere l'articolo della Knowledge base [come disabilitare la funzionalità di avvio automatico di Windows](https://support.microsoft.com/kb/967715) .</span><span class="sxs-lookup"><span data-stu-id="a2405-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="a2405-136">Questo articolo elenca i diversi aggiornamenti che è necessario avere installato per disabilitare correttamente la funzionalità di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="a2405-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="a2405-137">I valori NoDriveAutoRun e NoDriveTypeAutoRun devono essere modificati solo dagli amministratori di sistema per modificare il valore dell'intero sistema a scopo di test o amministrativo.</span><span class="sxs-lookup"><span data-stu-id="a2405-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="a2405-138">Le applicazioni non devono modificare questi valori, perché non è possibile ripristinare i valori originali in modo affidabile.</span><span class="sxs-lookup"><span data-stu-id="a2405-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="a2405-139">Il valore NoDriveAutoRun Disabilita l'esecuzione automatica per le lettere di unità specificate.</span><span class="sxs-lookup"><span data-stu-id="a2405-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="a2405-140">Si tratta di un \_ valore di dati reg DWORD, disponibile nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="a2405-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="a2405-141">Il primo bit del valore corrisponde all'unità a:, il secondo a B: e così via.</span><span class="sxs-lookup"><span data-stu-id="a2405-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="a2405-142">Per disabilitare l'esecuzione automatica per una o più lettere di unità, impostare i bit corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a2405-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="a2405-143">Per disabilitare ad esempio le unità A: e C:, impostare NoDriveAutoRun su `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="a2405-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="a2405-144">Il valore NoDriveTypeAutoRun Disabilita l'esecuzione automatica per una classe di unità.</span><span class="sxs-lookup"><span data-stu-id="a2405-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="a2405-145">Si tratta di un \_ valore reg DWORD o di dati binari reg a 4 byte \_ , disponibile nella stessa chiave.</span><span class="sxs-lookup"><span data-stu-id="a2405-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="a2405-146">Impostando i bit del primo byte di questo valore, è possibile escludere unità diverse dall'utilizzo dell'AutoRun.</span><span class="sxs-lookup"><span data-stu-id="a2405-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="a2405-147">Nella tabella seguente vengono fornite le costanti bits e maschera di bit, che possono essere impostate nel primo byte di NoDriveTypeAutoRun per disabilitare l'esecuzione automatica per un determinato tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="a2405-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="a2405-148">Per rendere effettive le modifiche, è necessario riavviare Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="a2405-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="a2405-149">Numero bit</span><span class="sxs-lookup"><span data-stu-id="a2405-149">Bit Number</span></span> | <span data-ttu-id="a2405-150">Costante maschera di maschera</span><span class="sxs-lookup"><span data-stu-id="a2405-150">Bitmask Constant</span></span>      | <span data-ttu-id="a2405-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2405-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="a2405-152">0x04</span><span class="sxs-lookup"><span data-stu-id="a2405-152">0x04</span></span>       | <span data-ttu-id="a2405-153">**UNITÀ \_ rimuovibile**</span><span class="sxs-lookup"><span data-stu-id="a2405-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="a2405-154">Il disco può essere rimosso dall'unità, ad esempio un disco floppy.</span><span class="sxs-lookup"><span data-stu-id="a2405-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="a2405-155">0x08</span><span class="sxs-lookup"><span data-stu-id="a2405-155">0x08</span></span>       | <span data-ttu-id="a2405-156">**UNITÀ \_ fissa**</span><span class="sxs-lookup"><span data-stu-id="a2405-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="a2405-157">Non è possibile rimuovere il disco dall'unità (disco rigido).</span><span class="sxs-lookup"><span data-stu-id="a2405-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="a2405-158">0x10</span><span class="sxs-lookup"><span data-stu-id="a2405-158">0x10</span></span>       | <span data-ttu-id="a2405-159">**UNITÀ \_ remota**</span><span class="sxs-lookup"><span data-stu-id="a2405-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="a2405-160">Unità di rete.</span><span class="sxs-lookup"><span data-stu-id="a2405-160">Network drive.</span></span>                                          |
| <span data-ttu-id="a2405-161">0x20</span><span class="sxs-lookup"><span data-stu-id="a2405-161">0x20</span></span>       | <span data-ttu-id="a2405-162">**UNITÀ \_ CD-ROM**</span><span class="sxs-lookup"><span data-stu-id="a2405-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="a2405-163">Unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="a2405-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="a2405-164">0x40</span><span class="sxs-lookup"><span data-stu-id="a2405-164">0x40</span></span>       | <span data-ttu-id="a2405-165">**UNITÀ \_ ramdisk**</span><span class="sxs-lookup"><span data-stu-id="a2405-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="a2405-166">Disco RAM.</span><span class="sxs-lookup"><span data-stu-id="a2405-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="a2405-167">AutoRun per altri tipi di supporti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a2405-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="a2405-168">AutoRun è destinato principalmente alla distribuzione pubblica di applicazioni su CD-ROM e DVD-ROM e il suo utilizzo è sconsigliato per altri supporti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a2405-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="a2405-169">Tuttavia, è spesso utile abilitare l'esecuzione automatica su altri tipi di supporti di archiviazione rimovibili.</span><span class="sxs-lookup"><span data-stu-id="a2405-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="a2405-170">Questa funzionalità viene in genere usata per semplificare il debug dei file AutoRun. inf.</span><span class="sxs-lookup"><span data-stu-id="a2405-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="a2405-171">AutoRun funziona solo nei dispositivi di archiviazione rimovibili quando vengono soddisfatti i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2405-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="a2405-172">Il dispositivo deve avere driver compatibili con l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="a2405-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="a2405-173">Per essere compatibile con l'AutoRun, un driver deve notificare al sistema che è stato inserito un disco inviando un messaggio [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a2405-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="a2405-174">La directory radice del supporto inserito deve contenere un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="a2405-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="a2405-175">L'AutoRun del dispositivo non deve essere disabilitato tramite il [Registro di sistema](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="a2405-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="a2405-176">L'applicazione in primo piano non ha [eliminato](#suppressing-autorun-programmatically) l'autorun.</span><span class="sxs-lookup"><span data-stu-id="a2405-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="a2405-177">Questa funzionalità non deve essere utilizzata per distribuire applicazioni su supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="a2405-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="a2405-178">Poiché l'implementazione dell'AutoRun su supporti rimovibili fornisce un modo semplice per diffondere i virus dei computer, gli utenti devono essere sospetti di qualsiasi disco floppy distribuito pubblicamente che contenga un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="a2405-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="a2405-179">In genere, l'esecuzione automatica viene avviata automaticamente, ma può anche essere avviata manualmente.</span><span class="sxs-lookup"><span data-stu-id="a2405-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="a2405-180">Se il dispositivo soddisfa i criteri elencati in precedenza, nel menu di scelta rapida della lettera di unità sarà incluso un comando **AutoPlay** .</span><span class="sxs-lookup"><span data-stu-id="a2405-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="a2405-181">Per eseguire l'esecuzione automatica manualmente, fare clic con il pulsante destro del mouse sull'icona dell'unità e scegliere **AutoPlay** dal menu di scelta rapida oppure fare doppio clic sull'icona dell'unità.</span><span class="sxs-lookup"><span data-stu-id="a2405-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="a2405-182">Se i driver non sono compatibili con l'AutoRun, il menu di scelta rapida non avrà un elemento **AutoPlay** e non sarà possibile avviare Autorun.</span><span class="sxs-lookup"><span data-stu-id="a2405-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="a2405-183">I driver compatibili con l'AutoRun sono forniti con alcune unità disco rimovibili, oltre ad altri tipi di supporti rimovibili, ad esempio schede CompactFlash.</span><span class="sxs-lookup"><span data-stu-id="a2405-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="a2405-184">AutoRun funziona anche con le unità di rete di cui è stato eseguito il mapping a una lettera di unità con Esplora risorse o montata con [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span><span class="sxs-lookup"><span data-stu-id="a2405-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="a2405-185">Come per l'hardware montato, un'unità di rete montata deve avere un file Autorun. inf nella directory radice e non deve essere disabilitata tramite il [Registro di sistema](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="a2405-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
