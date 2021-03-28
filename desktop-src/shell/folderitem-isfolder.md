---
description: Indica se l'elemento è una cartella.
ms.assetid: fb080c8f-04b1-4f9a-9219-0951a2e950ea
title: Proprietà FolderItem. Directory (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bf0bd4eb9b7964620fe705d6e8f4d10644ca234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977055"
---
# <a name="folderitemisfolder-property"></a><span data-ttu-id="d6c5c-103">Proprietà FolderItem. IsSynchronized</span><span class="sxs-lookup"><span data-stu-id="d6c5c-103">FolderItem.IsFolder property</span></span>

<span data-ttu-id="d6c5c-104">Indica se l'elemento è una cartella.</span><span class="sxs-lookup"><span data-stu-id="d6c5c-104">Indicates if the item is a folder.</span></span>

<span data-ttu-id="d6c5c-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6c5c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c5c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6c5c-106">Syntax</span></span>


```JScript
bIsFolder = FolderItem.IsFolder
```



## <a name="property-value"></a><span data-ttu-id="d6c5c-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6c5c-107">Property value</span></span>

<span data-ttu-id="d6c5c-108">**Valore booleano** che riceve **true** se l'elemento è una cartella o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d6c5c-108">A **Boolean** that receives **true** if the item is a folder or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="d6c5c-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6c5c-109">Examples</span></span>

<span data-ttu-id="d6c5c-110">Nell'esempio seguente viene utilizzata la **cartella** per determinare se la directory di Windows è una cartella.</span><span class="sxs-lookup"><span data-stu-id="d6c5c-110">The following example uses **IsFolder** to determine whether the Windows directory is a folder.</span></span> <span data-ttu-id="d6c5c-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d6c5c-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d6c5c-112">JScript</span><span class="sxs-lookup"><span data-stu-id="d6c5c-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFolder;
            }
        }
    }
</script>
```



<span data-ttu-id="d6c5c-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="d6c5c-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFolder
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d6c5c-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d6c5c-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFolder
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d6c5c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6c5c-115">Requirements</span></span>



| <span data-ttu-id="d6c5c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c5c-116">Requirement</span></span> | <span data-ttu-id="d6c5c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c5c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c5c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c5c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c5c-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d6c5c-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d6c5c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c5c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c5c-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6c5c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6c5c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6c5c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c5c-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c5c-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d6c5c-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d6c5c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6c5c-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6c5c-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d6c5c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c5c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c5c-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c5c-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




