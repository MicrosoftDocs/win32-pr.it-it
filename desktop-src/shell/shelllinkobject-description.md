---
description: Ottiene o imposta la descrizione del collegamento.
ms.assetid: d3a95281-fb1f-4fd4-9d26-2a6e10a36a86
title: Proprietà ShellLinkObject. Description (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Description
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aff08831bf194da5c7ce958e5a0746abdd533dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979831"
---
# <a name="shelllinkobjectdescription-property"></a><span data-ttu-id="4464f-103">Proprietà ShellLinkObject. Description</span><span class="sxs-lookup"><span data-stu-id="4464f-103">ShellLinkObject.Description property</span></span>

<span data-ttu-id="4464f-104">Ottiene o imposta la descrizione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="4464f-104">Gets or sets the description of the link.</span></span>

<span data-ttu-id="4464f-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4464f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4464f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4464f-106">Syntax</span></span>


```JScript
strDescription = ShellLinkObject.Description
ShellLinkObject.Description(sDescription) = strDescription
```



## <a name="property-value"></a><span data-ttu-id="4464f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4464f-107">Property value</span></span>

<span data-ttu-id="4464f-108">Descrizione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="4464f-108">the link's description.</span></span>

## <a name="examples"></a><span data-ttu-id="4464f-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="4464f-109">Examples</span></span>

<span data-ttu-id="4464f-110">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4464f-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4464f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4464f-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectDescriptionJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var szDescription;
                    
                    // Get the description for the ShellLinkObject.
                    szDescription = objShellLink.Description;
                    alert(szDescription);
                    
                    // Set the description for the ShellLinkObject.
                    objShellLink.Description = "Test"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="4464f-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="4464f-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectDescriptionVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szDescription
                                
                                'Get the description for the ShellLinkObject.
                                szDescription = objShellLink.Description
                                alert(szDescription)
                                
                                'Set the description for the ShellLinkObject.
                                objShellLink.Description = "Test"
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4464f-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4464f-113">Visual Basic:</span></span>


```VB
rivate Sub fnShellLinkObjectDescriptionVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szDescription As String
                            
                            'Get the description for the ShellLinkObject.
                            szDescription = objShellLink.Description
                            Debug.Print szDescription
                            
                            'Set the description for the ShellLinkObject.
                            objShellLink.Description = "Test"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4464f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4464f-114">Requirements</span></span>



| <span data-ttu-id="4464f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4464f-115">Requirement</span></span> | <span data-ttu-id="4464f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4464f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4464f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4464f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4464f-118">Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4464f-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4464f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4464f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4464f-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4464f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4464f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4464f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4464f-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4464f-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4464f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4464f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4464f-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4464f-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4464f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4464f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4464f-126"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4464f-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




