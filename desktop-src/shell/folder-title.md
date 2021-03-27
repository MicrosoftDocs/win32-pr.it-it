---
description: Contiene il titolo della cartella.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Proprietà Folder. title (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979682"
---
# <a name="foldertitle-property"></a><span data-ttu-id="4b05d-103">Proprietà Folder. title</span><span class="sxs-lookup"><span data-stu-id="4b05d-103">Folder.Title property</span></span>

<span data-ttu-id="4b05d-104">Contiene il titolo della cartella.</span><span class="sxs-lookup"><span data-stu-id="4b05d-104">Contains the title of the folder.</span></span>

<span data-ttu-id="4b05d-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4b05d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b05d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b05d-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="4b05d-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4b05d-107">Property value</span></span>

<span data-ttu-id="4b05d-108">Stringa che contiene il titolo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4b05d-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b05d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b05d-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b05d-110">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="4b05d-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="4b05d-111">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="4b05d-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="4b05d-112">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="4b05d-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4b05d-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="4b05d-113">Examples</span></span>

<span data-ttu-id="4b05d-114">Nell'esempio seguente viene usato **title** per recuperare il titolo della cartella che contiene i gruppi di programmi dell'utente (in genere "programmi").</span><span class="sxs-lookup"><span data-stu-id="4b05d-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="4b05d-115">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b05d-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4b05d-116">JScript</span><span class="sxs-lookup"><span data-stu-id="4b05d-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="4b05d-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="4b05d-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4b05d-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4b05d-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4b05d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b05d-119">Requirements</span></span>



| <span data-ttu-id="4b05d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b05d-120">Requirement</span></span> | <span data-ttu-id="4b05d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4b05d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b05d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b05d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b05d-123">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b05d-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b05d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b05d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b05d-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b05d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b05d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b05d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b05d-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b05d-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4b05d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4b05d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b05d-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b05d-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4b05d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b05d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b05d-131"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4b05d-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




