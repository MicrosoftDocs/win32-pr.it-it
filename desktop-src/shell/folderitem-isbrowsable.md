---
description: Indica se l'elemento può essere ospitato all'interno di un browser o di un frame di Esplora risorse.
ms.assetid: 472e0906-9561-4390-a503-c5e490245ea0
title: Proprietà FolderItem. navigable (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsBrowsable
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d7c5f7a9cbde54647c299646bb6350c3be6aa2a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401522"
---
# <a name="folderitemisbrowsable-property"></a><span data-ttu-id="a8e22-103">Proprietà FolderItem. navigable</span><span class="sxs-lookup"><span data-stu-id="a8e22-103">FolderItem.IsBrowsable property</span></span>

<span data-ttu-id="a8e22-104">Indica se l'elemento può essere ospitato all'interno di un browser o di un frame di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="a8e22-104">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span>

<span data-ttu-id="a8e22-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a8e22-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e22-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8e22-106">Syntax</span></span>


```JScript
bIsBrowsable = FolderItem.IsBrowsable
```



## <a name="property-value"></a><span data-ttu-id="a8e22-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a8e22-107">Property value</span></span>

<span data-ttu-id="a8e22-108">**Valore booleano** che riceve **true** se l'elemento può essere esplorato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8e22-108">A **Boolean** that receives **true** if the item can be browsed or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="a8e22-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8e22-109">Examples</span></span>

<span data-ttu-id="a8e22-110">Nell'esempio seguente viene usato l'oggetto **navigable** per determinare lo stato esplorabile della cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="a8e22-110">The following example uses **IsBrowsable** to determine the browsable state of the Windows folder.</span></span> <span data-ttu-id="a8e22-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a8e22-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a8e22-112">JScript</span><span class="sxs-lookup"><span data-stu-id="a8e22-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsBrowsableJ()
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
                
                bReturn = objFolderItem.IsBrowsable;
            }
        }
    }
</script>
```



<span data-ttu-id="a8e22-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="a8e22-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsBrowsableVB()
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
                                
                    bReturn = objFolderItem.IsBrowsable
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a8e22-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a8e22-114">Visual Basic:</span></span>


```VB
Private Sub fnIsBrowsableVB()
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
                    
                    bReturn = objFolderItem.IsBrowsable
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



## <a name="requirements"></a><span data-ttu-id="a8e22-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8e22-115">Requirements</span></span>



| <span data-ttu-id="a8e22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e22-116">Requirement</span></span> | <span data-ttu-id="a8e22-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a8e22-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e22-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8e22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e22-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8e22-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8e22-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8e22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e22-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8e22-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8e22-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8e22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e22-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e22-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a8e22-124">IDL</span><span class="sxs-lookup"><span data-stu-id="a8e22-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8e22-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8e22-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a8e22-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e22-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e22-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a8e22-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




