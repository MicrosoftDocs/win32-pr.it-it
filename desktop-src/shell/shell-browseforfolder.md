---
description: "Metodo Shell.BrowseForFolder: crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto Folder della cartella selezionata."
title: Metodo Shell.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: e5ec05ab09c7592e976085c230a2b359091fb819
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104369"
---
# <a name="shellbrowseforfolder-method"></a><span data-ttu-id="c0315-103">Metodo Shell.BrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="c0315-103">Shell.BrowseForFolder method</span></span>

<span data-ttu-id="c0315-104">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto [**Cartella della cartella**](folder.md) selezionata.</span><span class="sxs-lookup"><span data-stu-id="c0315-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0315-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0315-105">Syntax</span></span>


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="c0315-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0315-107">*Hwnd* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c0315-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0315-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="c0315-108">Type: **Integer**</span></span>

<span data-ttu-id="c0315-109">Handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0315-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="c0315-110">Il valore può essere zero.</span><span class="sxs-lookup"><span data-stu-id="c0315-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0315-111">*sTitle* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c0315-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0315-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c0315-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c0315-113">Valore **String** che rappresenta il titolo visualizzato all'interno della **finestra di** dialogo Sfoglia.</span><span class="sxs-lookup"><span data-stu-id="c0315-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="c0315-114">*iOptions* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c0315-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0315-115">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="c0315-115">Type: **Integer**</span></span>

<span data-ttu-id="c0315-116">Valore **Integer** che contiene le opzioni per il metodo.</span><span class="sxs-lookup"><span data-stu-id="c0315-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="c0315-117">Può essere zero o una combinazione dei valori elencati nel membro **ulFlags** della [**struttura BROWSEINFO.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)</span><span class="sxs-lookup"><span data-stu-id="c0315-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0315-118">*vRootFolder* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c0315-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0315-119">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="c0315-119">Type: **Variant**</span></span>

<span data-ttu-id="c0315-120">Cartella radice da utilizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0315-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="c0315-121">L'utente non può spostarsi più in alto nell'albero rispetto a questa cartella.</span><span class="sxs-lookup"><span data-stu-id="c0315-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="c0315-122">Se questo valore non viene specificato, la cartella radice usata nella finestra di dialogo è il desktop.</span><span class="sxs-lookup"><span data-stu-id="c0315-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="c0315-123">Questo valore può essere una stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="c0315-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="c0315-124">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="c0315-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="c0315-125">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="c0315-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0315-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0315-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c0315-127">JScript</span><span class="sxs-lookup"><span data-stu-id="c0315-127">JScript</span></span>

<span data-ttu-id="c0315-128">Tipo: **\* \* CARTELLA**</span><span class="sxs-lookup"><span data-stu-id="c0315-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="c0315-129">Riferimento a un oggetto all'oggetto [**Folder della cartella**](folder.md) selezionata.</span><span class="sxs-lookup"><span data-stu-id="c0315-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="c0315-130">VB</span><span class="sxs-lookup"><span data-stu-id="c0315-130">VB</span></span>

<span data-ttu-id="c0315-131">Tipo: **\* \* CARTELLA**</span><span class="sxs-lookup"><span data-stu-id="c0315-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="c0315-132">Riferimento a un oggetto all'oggetto [**Folder della cartella**](folder.md) selezionata.</span><span class="sxs-lookup"><span data-stu-id="c0315-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="c0315-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0315-133">Examples</span></span>

<span data-ttu-id="c0315-134">L'esempio seguente **usa BrowseForFolder** per visualizzare una finestra di esplorazione denominata "Example" radice nella cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="c0315-134">The following example uses **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="c0315-135">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c0315-135">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c0315-136">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c0315-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="c0315-137">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="c0315-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c0315-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c0315-138">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c0315-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0315-139">Requirements</span></span>



| <span data-ttu-id="c0315-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0315-140">Requirement</span></span> | <span data-ttu-id="c0315-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c0315-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0315-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0315-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c0315-143">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c0315-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c0315-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0315-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c0315-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0315-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0315-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0315-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0315-147"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0315-147"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c0315-148">Idl</span><span class="sxs-lookup"><span data-stu-id="c0315-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0315-149"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0315-149"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c0315-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c0315-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0315-151"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c0315-151"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
