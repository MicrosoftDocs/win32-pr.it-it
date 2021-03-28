---
description: Sposta un elemento o elementi in questa cartella.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Metodo Folder. MoveHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749178"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="bff56-103">Folder. MoveHere, metodo</span><span class="sxs-lookup"><span data-stu-id="bff56-103">Folder.MoveHere method</span></span>

<span data-ttu-id="bff56-104">Sposta un elemento o elementi in questa cartella.</span><span class="sxs-lookup"><span data-stu-id="bff56-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bff56-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="bff56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bff56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff56-107">*vite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bff56-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bff56-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bff56-108">Type: **Variant**</span></span>

<span data-ttu-id="bff56-109">Elemento o elementi da spostare.</span><span class="sxs-lookup"><span data-stu-id="bff56-109">The item or items to move.</span></span> <span data-ttu-id="bff56-110">Può trattarsi di una stringa che rappresenta un nome file, un oggetto [**FolderItem**](folderitem.md) o un oggetto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="bff56-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="bff56-111">*vOptions* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bff56-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bff56-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bff56-112">Type: **Variant**</span></span>

<span data-ttu-id="bff56-113">Opzioni per l'operazione di spostamento.</span><span class="sxs-lookup"><span data-stu-id="bff56-113">Options for the move operation.</span></span> <span data-ttu-id="bff56-114">Questo valore può essere zero o una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bff56-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="bff56-115">Questi valori sono basati su flag definiti per l'uso con il membro **fFlags** della struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) di C++.</span><span class="sxs-lookup"><span data-stu-id="bff56-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="bff56-116">Questi flag non sono definiti come tali per Visual Basic, VBScript o JScript, quindi è necessario definirli autonomamente o utilizzarne gli equivalenti numerici.</span><span class="sxs-lookup"><span data-stu-id="bff56-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="bff56-117">(4)</span><span class="sxs-lookup"><span data-stu-id="bff56-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-118">Non visualizzare una finestra di dialogo di stato.</span><span class="sxs-lookup"><span data-stu-id="bff56-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-119">(8)</span><span class="sxs-lookup"><span data-stu-id="bff56-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-120">Assegnare al file un nuovo nome in un'operazione di spostamento, copia o ridenominazione se esiste già un file con il nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bff56-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-121">(16)</span><span class="sxs-lookup"><span data-stu-id="bff56-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-122">Rispondere con "Sì a tutti" per qualsiasi finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="bff56-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-123">(64)</span><span class="sxs-lookup"><span data-stu-id="bff56-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-124">Mantenere le informazioni di annullamento, se possibile.</span><span class="sxs-lookup"><span data-stu-id="bff56-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-125">(128)</span><span class="sxs-lookup"><span data-stu-id="bff56-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-126">Eseguire l'operazione sui file solo se viene specificato un nome file con caratteri jolly ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="bff56-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-127">(256)</span><span class="sxs-lookup"><span data-stu-id="bff56-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-128">Visualizza una finestra di dialogo di stato ma non Mostra i nomi dei file.</span><span class="sxs-lookup"><span data-stu-id="bff56-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-129">(512)</span><span class="sxs-lookup"><span data-stu-id="bff56-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-130">Non confermare la creazione di una nuova directory se l'operazione ne richiede la creazione.</span><span class="sxs-lookup"><span data-stu-id="bff56-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="bff56-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-132">Se si verifica un errore, non visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bff56-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="bff56-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="bff56-134">Versione 4,71.</span><span class="sxs-lookup"><span data-stu-id="bff56-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="bff56-135">Non copiare gli attributi di sicurezza del file.</span><span class="sxs-lookup"><span data-stu-id="bff56-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="bff56-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="bff56-137">Utilizzare solo nella directory locale.</span><span class="sxs-lookup"><span data-stu-id="bff56-137">Only operate in the local directory.</span></span> <span data-ttu-id="bff56-138">Non funzionano in modo ricorsivo nelle sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="bff56-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="bff56-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="bff56-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="bff56-140">Versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="bff56-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="bff56-141">Non spostare i file connessi come gruppo.</span><span class="sxs-lookup"><span data-stu-id="bff56-141">Do not move connected files as a group.</span></span> <span data-ttu-id="bff56-142">Spostare solo i file specificati.</span><span class="sxs-lookup"><span data-stu-id="bff56-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff56-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bff56-143">Return value</span></span>

<span data-ttu-id="bff56-144">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bff56-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff56-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="bff56-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bff56-146">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="bff56-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="bff56-147">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="bff56-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="bff56-148">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="bff56-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bff56-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="bff56-149">Examples</span></span>

<span data-ttu-id="bff56-150">Nell'esempio seguente viene usato **MoveHere** per spostare il file Temp.txt dalla directory radice dell'unità c alla cartella c: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="bff56-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="bff56-151">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bff56-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bff56-152">JScript</span><span class="sxs-lookup"><span data-stu-id="bff56-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="bff56-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="bff56-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="bff56-154">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bff56-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bff56-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bff56-155">Requirements</span></span>



| <span data-ttu-id="bff56-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff56-156">Requirement</span></span> | <span data-ttu-id="bff56-157">Valore</span><span class="sxs-lookup"><span data-stu-id="bff56-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff56-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bff56-158">Minimum supported client</span></span><br/> | <span data-ttu-id="bff56-159">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bff56-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bff56-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bff56-160">Minimum supported server</span></span><br/> | <span data-ttu-id="bff56-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bff56-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bff56-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bff56-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff56-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff56-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bff56-164">IDL</span><span class="sxs-lookup"><span data-stu-id="bff56-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bff56-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bff56-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bff56-166">DLL</span><span class="sxs-lookup"><span data-stu-id="bff56-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bff56-167"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bff56-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




