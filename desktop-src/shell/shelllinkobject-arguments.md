---
description: Contiene gli argomenti di un collegamento.
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: Proprietà ShellLinkObject. Arguments (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c9b8a32eb4b935b5164ef91bf299777b36d7e53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233191"
---
# <a name="shelllinkobjectarguments-property"></a><span data-ttu-id="7a8fc-103">Proprietà ShellLinkObject. Arguments</span><span class="sxs-lookup"><span data-stu-id="7a8fc-103">ShellLinkObject.Arguments property</span></span>

<span data-ttu-id="7a8fc-104">Contiene gli argomenti di un collegamento.</span><span class="sxs-lookup"><span data-stu-id="7a8fc-104">Contains a link's arguments.</span></span>

<span data-ttu-id="7a8fc-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7a8fc-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8fc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a8fc-106">Syntax</span></span>


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a><span data-ttu-id="7a8fc-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7a8fc-107">Property value</span></span>

<span data-ttu-id="7a8fc-108">argomenti del collegamento.</span><span class="sxs-lookup"><span data-stu-id="7a8fc-108">the link's arguments.</span></span>

## <a name="examples"></a><span data-ttu-id="7a8fc-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a8fc-109">Examples</span></span>

<span data-ttu-id="7a8fc-110">Nell'esempio seguente vengono utilizzati gli **argomenti** per recuperare gli argomenti per un collegamento a Internet Explorer disponibile nel menu Start dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7a8fc-110">The following example uses **Arguments** to retrieve the arguments for a link to Internet Explorer found in the user's Start menu.</span></span> <span data-ttu-id="7a8fc-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7a8fc-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7a8fc-112">JScript</span><span class="sxs-lookup"><span data-stu-id="7a8fc-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="7a8fc-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="7a8fc-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
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
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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



<span data-ttu-id="7a8fc-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7a8fc-114">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectArgumentsVB()
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
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                End If

                Set objShellLink = Nothing
            End If

            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7a8fc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a8fc-115">Requirements</span></span>



| <span data-ttu-id="7a8fc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a8fc-116">Requirement</span></span> | <span data-ttu-id="7a8fc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7a8fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8fc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a8fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8fc-119">Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="7a8fc-119">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7a8fc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a8fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8fc-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a8fc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7a8fc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a8fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a8fc-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fc-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7a8fc-124">IDL</span><span class="sxs-lookup"><span data-stu-id="7a8fc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a8fc-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fc-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7a8fc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7a8fc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a8fc-127"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fc-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




