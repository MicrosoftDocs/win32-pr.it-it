---
description: Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto cartella della cartella selezionata.
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Metodo IShellDispatch. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e603bb08b4b98ba4008aa4ea162c9b59e5d42da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130102"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="bc049-103">IShellDispatch. BrowseForFolder, metodo</span><span class="sxs-lookup"><span data-stu-id="bc049-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="bc049-104">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto [**cartella**](folder.md) della cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="bc049-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc049-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc049-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="bc049-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc049-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc049-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc049-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="bc049-108">Type: **Integer**</span></span>

<span data-ttu-id="bc049-109">Handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bc049-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="bc049-110">Il valore può essere zero.</span><span class="sxs-lookup"><span data-stu-id="bc049-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc049-111">*sTitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc049-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc049-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="bc049-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="bc049-113">Valore **stringa** che rappresenta il titolo visualizzato nella finestra di dialogo **Sfoglia** .</span><span class="sxs-lookup"><span data-stu-id="bc049-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="bc049-114">*iOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc049-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc049-115">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="bc049-115">Type: **Integer**</span></span>

<span data-ttu-id="bc049-116">Valore **intero** che contiene le opzioni per il metodo.</span><span class="sxs-lookup"><span data-stu-id="bc049-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="bc049-117">Può essere zero o una combinazione dei valori elencati sotto il membro **ulFlags** della struttura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="bc049-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bc049-118">*vRootFolder* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bc049-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc049-119">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bc049-119">Type: **Variant**</span></span>

<span data-ttu-id="bc049-120">Cartella radice da utilizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bc049-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="bc049-121">L'utente non può spostarsi più in alto nell'albero rispetto a questa cartella.</span><span class="sxs-lookup"><span data-stu-id="bc049-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="bc049-122">Se questo valore non viene specificato, la cartella radice utilizzata nella finestra di dialogo è il desktop.</span><span class="sxs-lookup"><span data-stu-id="bc049-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="bc049-123">Questo valore può essere una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="bc049-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="bc049-124">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="bc049-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="bc049-125">In questi casi, i valori numerici devono essere usati al suo posto.</span><span class="sxs-lookup"><span data-stu-id="bc049-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc049-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc049-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bc049-127">JScript</span><span class="sxs-lookup"><span data-stu-id="bc049-127">JScript</span></span>

<span data-ttu-id="bc049-128">Tipo: **cartella \* \***</span><span class="sxs-lookup"><span data-stu-id="bc049-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="bc049-129">Riferimento all'oggetto [**Folder**](folder.md) della cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="bc049-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="bc049-130">VB</span><span class="sxs-lookup"><span data-stu-id="bc049-130">VB</span></span>

<span data-ttu-id="bc049-131">Tipo: **cartella \* \***</span><span class="sxs-lookup"><span data-stu-id="bc049-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="bc049-132">Riferimento all'oggetto [**Folder**](folder.md) della cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="bc049-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc049-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc049-133">Remarks</span></span>

<span data-ttu-id="bc049-134">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. BrowseForFolder**](shell-browseforfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="bc049-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="bc049-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc049-135">Examples</span></span>

<span data-ttu-id="bc049-136">Gli esempi seguenti usano **BrowseForFolder** per visualizzare una finestra di esplorazione denominata "example" con radice nella cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="bc049-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="bc049-137">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bc049-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bc049-138">JScript</span><span class="sxs-lookup"><span data-stu-id="bc049-138">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="bc049-139">VBScript</span><span class="sxs-lookup"><span data-stu-id="bc049-139">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bc049-140">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bc049-140">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bc049-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc049-141">Requirements</span></span>



| <span data-ttu-id="bc049-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc049-142">Requirement</span></span> | <span data-ttu-id="bc049-143">Valore</span><span class="sxs-lookup"><span data-stu-id="bc049-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc049-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc049-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bc049-145">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bc049-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bc049-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc049-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bc049-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc049-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bc049-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc049-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc049-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc049-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bc049-150">IDL</span><span class="sxs-lookup"><span data-stu-id="bc049-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc049-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc049-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bc049-152">DLL</span><span class="sxs-lookup"><span data-stu-id="bc049-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc049-153"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bc049-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
