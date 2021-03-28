---
description: Contiene l'oggetto cartella padre.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Proprietà Folder. ParentFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967450"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="3d635-103">Proprietà Folder. ParentFolder</span><span class="sxs-lookup"><span data-stu-id="3d635-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="3d635-104">Contiene l'oggetto [**cartella**](folder.md) padre.</span><span class="sxs-lookup"><span data-stu-id="3d635-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="3d635-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3d635-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d635-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d635-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="3d635-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3d635-107">Property value</span></span>

<span data-ttu-id="3d635-108">Riferimento all'oggetto ParentFolder.</span><span class="sxs-lookup"><span data-stu-id="3d635-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d635-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d635-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3d635-110">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="3d635-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="3d635-111">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="3d635-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="3d635-112">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="3d635-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3d635-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="3d635-113">Examples</span></span>

<span data-ttu-id="3d635-114">Nell'esempio seguente viene illustrato l'utilizzo corretto di **ParentFolder** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3d635-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3d635-115">JScript</span><span class="sxs-lookup"><span data-stu-id="3d635-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="3d635-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="3d635-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3d635-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3d635-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3d635-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d635-118">Requirements</span></span>



| <span data-ttu-id="3d635-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d635-119">Requirement</span></span> | <span data-ttu-id="3d635-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3d635-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d635-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d635-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d635-122">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3d635-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d635-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d635-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d635-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d635-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d635-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d635-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d635-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d635-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3d635-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3d635-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d635-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d635-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3d635-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3d635-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d635-130"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3d635-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




