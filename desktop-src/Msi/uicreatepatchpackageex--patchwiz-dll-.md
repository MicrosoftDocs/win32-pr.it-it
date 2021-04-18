---
description: La funzione UiCreatePatchPackageEx accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp). La chiamata di Msimsp.exe è il metodo consigliato per l'utilizzo di Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305626"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="1c428-104">UiCreatePatchPackageEx (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="1c428-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="1c428-105">La funzione UiCreatePatchPackageEx accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp).</span><span class="sxs-lookup"><span data-stu-id="1c428-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="1c428-106">La chiamata di [Msimsp.exe](msimsp-exe.md) è il metodo consigliato per l'utilizzo di [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="1c428-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="1c428-107">La funzione UiCreatePatchPackageEx è disponibile a partire dalla versione Patchwiz.dll 4,0 ed estende la funzionalità della funzione [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="1c428-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="1c428-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c428-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c428-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="1c428-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-110">Percorso completo del file delle proprietà di creazione della patch (file con estensione PCP) per questa patch.</span><span class="sxs-lookup"><span data-stu-id="1c428-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="1c428-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="1c428-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-112">Percorso completo del pacchetto di patch Windows Installer (file con estensione msp) da creare.</span><span class="sxs-lookup"><span data-stu-id="1c428-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="1c428-113">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="1c428-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="1c428-114">Se è **null** o una stringa vuota, la funzione utilizza il valore di PatchOutputPath nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="1c428-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c428-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="1c428-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-116">Percorso completo di un file di log di testo che verrà accodato.</span><span class="sxs-lookup"><span data-stu-id="1c428-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="1c428-117">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="1c428-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="1c428-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="1c428-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-119">Handle per una finestra che Visualizza il testo dello stato.</span><span class="sxs-lookup"><span data-stu-id="1c428-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="1c428-120">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="1c428-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="1c428-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="1c428-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-122">Percorso dei file temporanei.</span><span class="sxs-lookup"><span data-stu-id="1c428-122">Location for temporary files.</span></span> <span data-ttu-id="1c428-123">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="1c428-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="1c428-124">L'utente deve disporre di privilegi sufficienti per la lettura e la scrittura in questa cartella.</span><span class="sxs-lookup"><span data-stu-id="1c428-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="1c428-125">Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="1c428-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="1c428-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="1c428-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-127">Se **true**, rimuovere la cartella temporanea e tutti i relativi contenuti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="1c428-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="1c428-128">Se **false** e la cartella è presente, la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1c428-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="1c428-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1c428-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-130">Questo parametro può essere impostato su uno o una combinazione dei valori seguenti per specificare le opzioni di registrazione o dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1c428-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="1c428-131">Flag</span><span class="sxs-lookup"><span data-stu-id="1c428-131">Flag</span></span>            | <span data-ttu-id="1c428-132">valore</span><span class="sxs-lookup"><span data-stu-id="1c428-132">Value</span></span>       | <span data-ttu-id="1c428-133">Significato</span><span class="sxs-lookup"><span data-stu-id="1c428-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="1c428-134">LOGNONE</span><span class="sxs-lookup"><span data-stu-id="1c428-134">LOGNONE</span></span>         | <span data-ttu-id="1c428-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c428-135">0x00000000</span></span>  | <span data-ttu-id="1c428-136">Non scrivere alcun messaggio nel log.</span><span class="sxs-lookup"><span data-stu-id="1c428-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="1c428-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="1c428-137">LOGINFO</span></span>         | <span data-ttu-id="1c428-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1c428-138">0x00000001</span></span>  | <span data-ttu-id="1c428-139">Scrivere messaggi informativi nel log.</span><span class="sxs-lookup"><span data-stu-id="1c428-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="1c428-140">LOGWARN</span><span class="sxs-lookup"><span data-stu-id="1c428-140">LOGWARN</span></span>         | <span data-ttu-id="1c428-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1c428-141">0x00000002</span></span>  | <span data-ttu-id="1c428-142">Scrivere gli avvisi nel log.</span><span class="sxs-lookup"><span data-stu-id="1c428-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="1c428-143">LOGERR</span><span class="sxs-lookup"><span data-stu-id="1c428-143">LOGERR</span></span>          | <span data-ttu-id="1c428-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1c428-144">0x00000004</span></span>  | <span data-ttu-id="1c428-145">Scrivere i messaggi di errore nel log.</span><span class="sxs-lookup"><span data-stu-id="1c428-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="1c428-146">LOGPERFMESSAGES</span><span class="sxs-lookup"><span data-stu-id="1c428-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="1c428-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1c428-147">0x00000008</span></span>  | <span data-ttu-id="1c428-148">Scrivere i messaggi relativi alle prestazioni nel log.</span><span class="sxs-lookup"><span data-stu-id="1c428-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="1c428-149">UINONE</span><span class="sxs-lookup"><span data-stu-id="1c428-149">UINONE</span></span>          | <span data-ttu-id="1c428-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="1c428-150">0x00000000f</span></span> | <span data-ttu-id="1c428-151">Non visualizzare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1c428-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="1c428-152">UIALL</span><span class="sxs-lookup"><span data-stu-id="1c428-152">UIALL</span></span>           | <span data-ttu-id="1c428-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c428-153">0x00000010</span></span>  | <span data-ttu-id="1c428-154">Visualizzare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1c428-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="1c428-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="1c428-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="1c428-156">Riservato.</span><span class="sxs-lookup"><span data-stu-id="1c428-156">Reserved.</span></span> <span data-ttu-id="1c428-157">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="1c428-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="1c428-158">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="1c428-158">Return Values</span></span>

<span data-ttu-id="1c428-159">Vedere la tabella in [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1c428-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c428-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c428-160">Remarks</span></span>

<span data-ttu-id="1c428-161">Per un esempio di creazione di un file con estensione PCP e uso di [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) per generare un pacchetto di patch di Windows Installer, vedere la sezione esempio di applicazione di [patch per un piccolo aggiornamento](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="1c428-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="1c428-162">Per la creazione di una patch è necessaria un'immagine di installazione non compressa, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="1c428-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="1c428-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) non genera patch binarie per i file nei file CAB.</span><span class="sxs-lookup"><span data-stu-id="1c428-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



