---
description: Ottiene o imposta il percorso dell'oggetto collegamento.
ms.assetid: ddb5be91-7c21-46c8-949e-bdd973e11b6c
title: Proprietà ShellLinkObject. Path (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Path
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac6b6f1168724f3808462088dc7e5907ec0cec58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234210"
---
# <a name="shelllinkobjectpath-property"></a><span data-ttu-id="5540c-103">Proprietà ShellLinkObject. Path</span><span class="sxs-lookup"><span data-stu-id="5540c-103">ShellLinkObject.Path property</span></span>

<span data-ttu-id="5540c-104">Ottiene o imposta il percorso dell'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="5540c-104">Gets or sets the path to the link object.</span></span>

<span data-ttu-id="5540c-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5540c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5540c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5540c-106">Syntax</span></span>


```JScript
strPath = ShellLinkObject.Path
ShellLinkObject.Path(sPath) = strPath
```



## <a name="property-value"></a><span data-ttu-id="5540c-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5540c-107">Property value</span></span>

<span data-ttu-id="5540c-108">percorso completo dell'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="5540c-108">the fully qualified path of the link object.</span></span>

## <a name="examples"></a><span data-ttu-id="5540c-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="5540c-109">Examples</span></span>

<span data-ttu-id="5540c-110">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5540c-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5540c-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5540c-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectPathJ()
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
                    var szPath;
                    
                    // Get the path for the ShellLinkObject.
                    szPath = objShellLink.Path;
                    alert(szPath);
                    
                    // Set the path for the ShellLinkObject.
                    objShellLink.Path = "C:\\Program Files\\IE\\IEXPLORE.EXE";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="5540c-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="5540c-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectPathVB()
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
                                dim szPath
                                
                                'Get the path for the ShellLinkObject..
                                szPath = objShellLink.Path
                                alert(szPath)
                                
                                'Set the path for the ShellLinkObject
                                objShellLink.Path = "C:\Program Files\IE\IEXPLORE.EXE"
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



<span data-ttu-id="5540c-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5540c-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectPathVB()
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
                            Dim szPath As String
                            
                            'Get the path for the ShellLinkObject.
                            szPath = objShellLink.Path
                            Debug.Print szPath
                            
                            'Set the path for the ShellLinkObject.
                            objShellLink.Path = "C:\Program Files\IE\IEXPLORE.EXE"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5540c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5540c-114">Requirements</span></span>



| <span data-ttu-id="5540c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5540c-115">Requirement</span></span> | <span data-ttu-id="5540c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5540c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5540c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5540c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5540c-118">Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5540c-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5540c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5540c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5540c-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5540c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5540c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5540c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5540c-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5540c-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5540c-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5540c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5540c-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5540c-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5540c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5540c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5540c-126"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5540c-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




