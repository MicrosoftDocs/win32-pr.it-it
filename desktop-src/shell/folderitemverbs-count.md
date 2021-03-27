---
description: Contiene il numero di elementi nella raccolta.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Proprietà FolderItemVerbs. Count (shldisp. h)
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
ms.openlocfilehash: b41e78261dfc9bc72e9262615bc395a9d559e33a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994720"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="c6a9a-103">Proprietà FolderItemVerbs. Count</span><span class="sxs-lookup"><span data-stu-id="c6a9a-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="c6a9a-104">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="c6a9a-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a9a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6a9a-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="c6a9a-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c6a9a-107">Property value</span></span>

<span data-ttu-id="c6a9a-108">**Intero** che riceve la proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="c6a9a-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="c6a9a-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="c6a9a-109">Examples</span></span>

<span data-ttu-id="c6a9a-110">Nell'esempio seguente viene usato **count** per recuperare il numero di verbi disponibili per la cartella del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="c6a9a-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c6a9a-112">JScript</span><span class="sxs-lookup"><span data-stu-id="c6a9a-112">JScript:</span></span>


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



<span data-ttu-id="c6a9a-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="c6a9a-113">VBScript:</span></span>


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



<span data-ttu-id="c6a9a-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c6a9a-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c6a9a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6a9a-115">Requirements</span></span>



| <span data-ttu-id="c6a9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a9a-116">Requirement</span></span> | <span data-ttu-id="c6a9a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a9a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a9a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a9a-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c6a9a-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6a9a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a9a-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6a9a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6a9a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6a9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6a9a-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6a9a-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c6a9a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c6a9a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6a9a-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6a9a-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c6a9a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c6a9a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6a9a-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c6a9a-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




