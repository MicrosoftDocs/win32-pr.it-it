---
description: Contiene l'oggetto FolderItem della cartella.
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: Proprietà Cartella2. self (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225796"
---
# <a name="folder2self-property"></a><span data-ttu-id="e3e2e-103">Proprietà Cartella2. self</span><span class="sxs-lookup"><span data-stu-id="e3e2e-103">Folder2.Self property</span></span>

<span data-ttu-id="e3e2e-104">Contiene l'oggetto [**FolderItem**](folderitem.md) della cartella.</span><span class="sxs-lookup"><span data-stu-id="e3e2e-104">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span>

<span data-ttu-id="e3e2e-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e3e2e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e2e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3e2e-106">Syntax</span></span>


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a><span data-ttu-id="e3e2e-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e3e2e-107">Property value</span></span>

<span data-ttu-id="e3e2e-108">Oggetto che restituisce l'oggetto [**FolderItem**](folderitem.md) della cartella.</span><span class="sxs-lookup"><span data-stu-id="e3e2e-108">The object that evaluates to the folder's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="e3e2e-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="e3e2e-109">Examples</span></span>

<span data-ttu-id="e3e2e-110">Nell'esempio seguente viene usato **auto** per recuperare [**FolderItem**](folderitem.md) per la cartella C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="e3e2e-110">The following example uses **Self** to retrieve the [**FolderItem**](folderitem.md) for the C:\\Windows folder.</span></span> <span data-ttu-id="e3e2e-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e3e2e-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e3e2e-112">JScript</span><span class="sxs-lookup"><span data-stu-id="e3e2e-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="e3e2e-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="e3e2e-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="e3e2e-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e3e2e-114">Visual Basic:</span></span>


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e3e2e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3e2e-115">Requirements</span></span>



| <span data-ttu-id="e3e2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e2e-116">Requirement</span></span> | <span data-ttu-id="e3e2e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e3e2e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e2e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3e2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e2e-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e3e2e-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3e2e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3e2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e2e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3e2e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e3e2e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3e2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3e2e-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e2e-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e3e2e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="e3e2e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3e2e-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3e2e-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e3e2e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e3e2e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3e2e-127"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e2e-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e2e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3e2e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e2e-129">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="e3e2e-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="e3e2e-130">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="e3e2e-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




