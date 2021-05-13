---
description: Copia uno o più elementi in una cartella.
title: Metodo Folder.CopyHere (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842142"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="31e33-103">Metodo Folder.CopyHere</span><span class="sxs-lookup"><span data-stu-id="31e33-103">Folder.CopyHere method</span></span>

<span data-ttu-id="31e33-104">Copia uno o più elementi in una cartella.</span><span class="sxs-lookup"><span data-stu-id="31e33-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31e33-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="31e33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="31e33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e33-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="31e33-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="31e33-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="31e33-108">Type: **Variant**</span></span>

<span data-ttu-id="31e33-109">Elemento o elementi da copiare.</span><span class="sxs-lookup"><span data-stu-id="31e33-109">The item or items to copy.</span></span> <span data-ttu-id="31e33-110">Può trattarsi di una stringa che rappresenta un nome file, un [**oggetto FolderItem**](folderitem.md) o [**un oggetto FolderItems.**](folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="31e33-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="31e33-111">*vOptions* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="31e33-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31e33-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="31e33-112">Type: **Variant**</span></span>

<span data-ttu-id="31e33-113">Opzioni per l'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="31e33-113">Options for the copy operation.</span></span> <span data-ttu-id="31e33-114">Questo valore può essere zero o una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="31e33-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="31e33-115">Questi valori sono basati sui flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++.</span><span class="sxs-lookup"><span data-stu-id="31e33-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="31e33-116">Ogni spazio dei nomi della shell deve fornire la propria implementazione di questi flag e ogni spazio dei nomi può scegliere di ignorare alcuni o anche tutti questi flag.</span><span class="sxs-lookup"><span data-stu-id="31e33-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="31e33-117">Questi flag non sono definiti in base al nome per Visual Basic, VBScript o JScript, pertanto è necessario definirli manualmente o usare i relativi equivalenti numerici.</span><span class="sxs-lookup"><span data-stu-id="31e33-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="31e33-118">In alcuni casi, ad esempio i file compressi (zip), alcuni flag di opzione possono essere ignorati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="31e33-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="31e33-119">(4)</span><span class="sxs-lookup"><span data-stu-id="31e33-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-120">Non visualizzare una finestra di dialogo di stato.</span><span class="sxs-lookup"><span data-stu-id="31e33-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-121">(8)</span><span class="sxs-lookup"><span data-stu-id="31e33-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-122">Assegnare al file utilizzato un nuovo nome in un'operazione di spostamento, copia o ridenominazione se esiste già un file con il nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31e33-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-123">(16)</span><span class="sxs-lookup"><span data-stu-id="31e33-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-124">Rispondere con "Sì a tutti" per qualsiasi finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="31e33-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-125">(64)</span><span class="sxs-lookup"><span data-stu-id="31e33-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-126">Se possibile, mantenere le informazioni di annullamento.</span><span class="sxs-lookup"><span data-stu-id="31e33-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-127">(128)</span><span class="sxs-lookup"><span data-stu-id="31e33-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-128">Eseguire l'operazione sui file solo se è specificato un nome file con caratteri jolly ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="31e33-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-129">(256)</span><span class="sxs-lookup"><span data-stu-id="31e33-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-130">Visualizzare una finestra di dialogo di stato ma non visualizzare i nomi dei file.</span><span class="sxs-lookup"><span data-stu-id="31e33-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-131">(512)</span><span class="sxs-lookup"><span data-stu-id="31e33-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-132">Non confermare la creazione di una nuova directory se l'operazione ne richiede la creazione.</span><span class="sxs-lookup"><span data-stu-id="31e33-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="31e33-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-134">Non visualizzare un'interfaccia utente se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="31e33-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="31e33-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="31e33-136">Versione 4.71.</span><span class="sxs-lookup"><span data-stu-id="31e33-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="31e33-137">Non copiare gli attributi di sicurezza del file.</span><span class="sxs-lookup"><span data-stu-id="31e33-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="31e33-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="31e33-139">Operare solo nella directory locale.</span><span class="sxs-lookup"><span data-stu-id="31e33-139">Only operate in the local directory.</span></span> <span data-ttu-id="31e33-140">Non operare in modo ricorsivo nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="31e33-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="31e33-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="31e33-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="31e33-142">Versione 5.0.</span><span class="sxs-lookup"><span data-stu-id="31e33-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="31e33-143">Non copiare i file connessi come gruppo.</span><span class="sxs-lookup"><span data-stu-id="31e33-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="31e33-144">Copiare solo i file specificati.</span><span class="sxs-lookup"><span data-stu-id="31e33-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e33-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31e33-145">Return value</span></span>

<span data-ttu-id="31e33-146">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="31e33-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31e33-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="31e33-147">Remarks</span></span>

<span data-ttu-id="31e33-148">Non viene inviata alcuna notifica al programma chiamante per indicare che la copia è stata completata.</span><span class="sxs-lookup"><span data-stu-id="31e33-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="31e33-149">Non tutti i metodi vengono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="31e33-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="31e33-150">Ad esempio, il [**metodo ParseName**](folder-parsename.md) non è implementato per la cartella Pannello di controllo (CSIDL \_ CONTROLS).</span><span class="sxs-lookup"><span data-stu-id="31e33-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="31e33-151">Se si tenta di chiamare un metodo non implementato, viene generato 0x800A01BD errore di tipo decimale 445.</span><span class="sxs-lookup"><span data-stu-id="31e33-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="31e33-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="31e33-152">Examples</span></span>

<span data-ttu-id="31e33-153">L'esempio seguente **usa CopyHere** per copiare il file Autoexec.bat dalla directory radice alla directory C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="31e33-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="31e33-154">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31e33-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="31e33-155">Jscript:</span><span class="sxs-lookup"><span data-stu-id="31e33-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="31e33-156">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="31e33-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="31e33-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="31e33-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="31e33-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31e33-158">Requirements</span></span>



| <span data-ttu-id="31e33-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e33-159">Requirement</span></span> | <span data-ttu-id="31e33-160">Valore</span><span class="sxs-lookup"><span data-stu-id="31e33-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e33-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31e33-161">Minimum supported client</span></span><br/> | <span data-ttu-id="31e33-162">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="31e33-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31e33-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31e33-163">Minimum supported server</span></span><br/> | <span data-ttu-id="31e33-164">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="31e33-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31e33-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31e33-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e33-166"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="31e33-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="31e33-167">Idl</span><span class="sxs-lookup"><span data-stu-id="31e33-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31e33-168"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="31e33-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="31e33-169">DLL</span><span class="sxs-lookup"><span data-stu-id="31e33-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e33-170"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="31e33-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e33-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31e33-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e33-172">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="31e33-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




