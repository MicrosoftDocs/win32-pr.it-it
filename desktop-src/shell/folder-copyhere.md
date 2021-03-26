---
description: Copia un elemento o elementi in una cartella.
title: Metodo Folder. CopyHere (shldisp. h)
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
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994736"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="9bf26-103">Folder. CopyHere, metodo</span><span class="sxs-lookup"><span data-stu-id="9bf26-103">Folder.CopyHere method</span></span>

<span data-ttu-id="9bf26-104">Copia un elemento o elementi in una cartella.</span><span class="sxs-lookup"><span data-stu-id="9bf26-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf26-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bf26-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="9bf26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bf26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf26-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="9bf26-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="9bf26-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9bf26-108">Type: **Variant**</span></span>

<span data-ttu-id="9bf26-109">Elemento o elementi da copiare.</span><span class="sxs-lookup"><span data-stu-id="9bf26-109">The item or items to copy.</span></span> <span data-ttu-id="9bf26-110">Può trattarsi di una stringa che rappresenta un nome file, un oggetto [**FolderItem**](folderitem.md) o un oggetto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="9bf26-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9bf26-111">*vOptions* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="9bf26-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9bf26-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9bf26-112">Type: **Variant**</span></span>

<span data-ttu-id="9bf26-113">Opzioni per l'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="9bf26-113">Options for the copy operation.</span></span> <span data-ttu-id="9bf26-114">Questo valore può essere zero o una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bf26-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="9bf26-115">Questi valori sono basati su flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++.</span><span class="sxs-lookup"><span data-stu-id="9bf26-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="9bf26-116">Ogni spazio dei nomi della shell deve fornire la propria implementazione di questi flag e ogni spazio dei nomi può scegliere di ignorare alcuni o anche tutti questi flag.</span><span class="sxs-lookup"><span data-stu-id="9bf26-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="9bf26-117">Questi flag non sono definiti per nome per Visual Basic, VBScript o JScript, quindi è necessario definirli autonomamente o utilizzarne gli equivalenti numerici.</span><span class="sxs-lookup"><span data-stu-id="9bf26-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="9bf26-118">In alcuni casi, ad esempio file compressi (zip), alcuni flag di opzione possono essere ignorati dalla progettazione.</span><span class="sxs-lookup"><span data-stu-id="9bf26-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="9bf26-119">(4)</span><span class="sxs-lookup"><span data-stu-id="9bf26-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-120">Non visualizzare una finestra di dialogo di stato.</span><span class="sxs-lookup"><span data-stu-id="9bf26-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-121">(8)</span><span class="sxs-lookup"><span data-stu-id="9bf26-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-122">Assegnare al file un nuovo nome in un'operazione di spostamento, copia o ridenominazione se esiste già un file con il nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bf26-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-123">(16)</span><span class="sxs-lookup"><span data-stu-id="9bf26-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-124">Rispondere con "Sì a tutti" per qualsiasi finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="9bf26-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-125">(64)</span><span class="sxs-lookup"><span data-stu-id="9bf26-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-126">Mantenere le informazioni di annullamento, se possibile.</span><span class="sxs-lookup"><span data-stu-id="9bf26-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-127">(128)</span><span class="sxs-lookup"><span data-stu-id="9bf26-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-128">Eseguire l'operazione sui file solo se viene specificato un nome file con caratteri jolly ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="9bf26-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-129">(256)</span><span class="sxs-lookup"><span data-stu-id="9bf26-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-130">Visualizza una finestra di dialogo di stato ma non Mostra i nomi dei file.</span><span class="sxs-lookup"><span data-stu-id="9bf26-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-131">(512)</span><span class="sxs-lookup"><span data-stu-id="9bf26-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-132">Non confermare la creazione di una nuova directory se l'operazione ne richiede la creazione.</span><span class="sxs-lookup"><span data-stu-id="9bf26-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="9bf26-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-134">Se si verifica un errore, non visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9bf26-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="9bf26-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="9bf26-136">Versione 4,71.</span><span class="sxs-lookup"><span data-stu-id="9bf26-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="9bf26-137">Non copiare gli attributi di sicurezza del file.</span><span class="sxs-lookup"><span data-stu-id="9bf26-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="9bf26-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="9bf26-139">Utilizzare solo nella directory locale.</span><span class="sxs-lookup"><span data-stu-id="9bf26-139">Only operate in the local directory.</span></span> <span data-ttu-id="9bf26-140">Non funzionano in modo ricorsivo nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="9bf26-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="9bf26-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="9bf26-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="9bf26-142">Versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="9bf26-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="9bf26-143">Non copiare i file connessi come gruppo.</span><span class="sxs-lookup"><span data-stu-id="9bf26-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="9bf26-144">Copiare solo i file specificati.</span><span class="sxs-lookup"><span data-stu-id="9bf26-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf26-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bf26-145">Return value</span></span>

<span data-ttu-id="9bf26-146">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9bf26-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf26-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bf26-147">Remarks</span></span>

<span data-ttu-id="9bf26-148">Non viene fornita alcuna notifica al programma chiamante per indicare che la copia è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9bf26-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="9bf26-149">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="9bf26-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="9bf26-150">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="9bf26-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="9bf26-151">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="9bf26-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9bf26-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="9bf26-152">Examples</span></span>

<span data-ttu-id="9bf26-153">Nell'esempio seguente viene usato **CopyHere** per copiare il file di Autoexec.bat dalla directory radice alla directory C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="9bf26-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="9bf26-154">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9bf26-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9bf26-155">JScript</span><span class="sxs-lookup"><span data-stu-id="9bf26-155">JScript:</span></span>


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



<span data-ttu-id="9bf26-156">VBScript</span><span class="sxs-lookup"><span data-stu-id="9bf26-156">VBScript:</span></span>


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



<span data-ttu-id="9bf26-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9bf26-157">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9bf26-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bf26-158">Requirements</span></span>



| <span data-ttu-id="9bf26-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bf26-159">Requirement</span></span> | <span data-ttu-id="9bf26-160">Valore</span><span class="sxs-lookup"><span data-stu-id="9bf26-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf26-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bf26-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf26-162">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9bf26-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9bf26-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bf26-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf26-164">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9bf26-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9bf26-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bf26-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bf26-166"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf26-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9bf26-167">IDL</span><span class="sxs-lookup"><span data-stu-id="9bf26-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9bf26-168"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9bf26-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9bf26-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf26-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf26-170"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9bf26-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf26-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bf26-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf26-172">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="9bf26-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




