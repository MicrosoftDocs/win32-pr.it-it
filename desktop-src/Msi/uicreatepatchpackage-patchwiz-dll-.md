---
description: La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878545"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="de99d-103">UiCreatePatchPackage (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="de99d-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="de99d-104">La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp).</span><span class="sxs-lookup"><span data-stu-id="de99d-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="de99d-105">La chiamata di [Msimsp.exe](msimsp-exe.md) è il metodo consigliato per l'utilizzo di [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="de99d-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="de99d-106">La funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) è disponibile nella versione 4,0 di Patchwiz.dll ed estende la funzionalità della funzione UiCreatePatchPackage.</span><span class="sxs-lookup"><span data-stu-id="de99d-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="de99d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="de99d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de99d-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="de99d-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-109">Percorso completo del file delle proprietà di creazione della patch (file con estensione PCP) per questa patch.</span><span class="sxs-lookup"><span data-stu-id="de99d-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="de99d-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="de99d-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-111">Percorso completo del pacchetto di patch Windows Installer (file con estensione msp) da creare.</span><span class="sxs-lookup"><span data-stu-id="de99d-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="de99d-112">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="de99d-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="de99d-113">Se è **null** o una stringa vuota, la funzione utilizza il valore di PatchOutputPath nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="de99d-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="de99d-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="de99d-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-115">Percorso completo di un file di log di testo che verrà accodato.</span><span class="sxs-lookup"><span data-stu-id="de99d-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="de99d-116">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="de99d-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="de99d-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="de99d-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-118">Handle per una finestra che Visualizza il testo dello stato.</span><span class="sxs-lookup"><span data-stu-id="de99d-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="de99d-119">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="de99d-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="de99d-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="de99d-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-121">Percorso dei file temporanei.</span><span class="sxs-lookup"><span data-stu-id="de99d-121">Location for temporary files.</span></span> <span data-ttu-id="de99d-122">Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="de99d-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="de99d-123">Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="de99d-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="de99d-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="de99d-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="de99d-125">Se **true**, rimuovere la cartella temporanea e tutti i relativi contenuti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="de99d-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="de99d-126">Se **false** e la cartella è presente, la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="de99d-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="de99d-127">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="de99d-127">Return Values</span></span>

<span data-ttu-id="de99d-128">Vedere la tabella in [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de99d-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de99d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="de99d-129">Remarks</span></span>

<span data-ttu-id="de99d-130">Per un esempio di creazione di un file con estensione PCP e uso di UiCreatePatchPackage per generare un pacchetto di patch di Windows Installer, vedere la sezione esempio di applicazione di [patch per un piccolo aggiornamento](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="de99d-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="de99d-131">Per la creazione di una patch è necessaria un'immagine di installazione non compressa, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="de99d-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="de99d-132">UiCreatePatchPackage non genera patch binarie per i file nei file CAB.</span><span class="sxs-lookup"><span data-stu-id="de99d-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



