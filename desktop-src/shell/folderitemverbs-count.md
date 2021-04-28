---
description: 'Proprietà FolderItemVerbs.Count : contiene il numero di elementi nella raccolta.'
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Proprietà FolderItemVerbs.Count (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5545ea64da914188226fbdabf7cc6301baa695af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089549"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="7a846-103">FolderItemVerbs.Count - proprietà</span><span class="sxs-lookup"><span data-stu-id="7a846-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="7a846-104">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="7a846-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="7a846-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7a846-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a846-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a846-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="7a846-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7a846-107">Property value</span></span>

<span data-ttu-id="7a846-108">Integer **che** riceve la **proprietà Count.**</span><span class="sxs-lookup"><span data-stu-id="7a846-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="7a846-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a846-109">Examples</span></span>

<span data-ttu-id="7a846-110">Nell'esempio seguente viene **utilizzato Count** per recuperare il conteggio dei verbi disponibili per la Pannello di controllo cartella .</span><span class="sxs-lookup"><span data-stu-id="7a846-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="7a846-111">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7a846-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7a846-112">Jscript:</span><span class="sxs-lookup"><span data-stu-id="7a846-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="7a846-113">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="7a846-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7a846-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7a846-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7a846-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a846-115">Requirements</span></span>



| <span data-ttu-id="7a846-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a846-116">Requirement</span></span> | <span data-ttu-id="7a846-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7a846-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a846-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a846-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a846-119">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7a846-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7a846-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a846-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a846-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a846-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a846-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a846-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a846-123"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7a846-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7a846-124">Idl</span><span class="sxs-lookup"><span data-stu-id="7a846-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a846-125"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a846-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7a846-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7a846-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a846-127"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7a846-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




