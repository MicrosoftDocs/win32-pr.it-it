---
description: Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: Proprietà ShellLinkObject. ShowCommand (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995165"
---
# <a name="shelllinkobjectshowcommand-property"></a><span data-ttu-id="3a77c-103">Proprietà ShellLinkObject. ShowCommand</span><span class="sxs-lookup"><span data-stu-id="3a77c-103">ShellLinkObject.ShowCommand property</span></span>

<span data-ttu-id="3a77c-104">Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.</span><span class="sxs-lookup"><span data-stu-id="3a77c-104">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span>

<span data-ttu-id="3a77c-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3a77c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a77c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a77c-106">Syntax</span></span>


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a><span data-ttu-id="3a77c-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3a77c-107">Property value</span></span>

<span data-ttu-id="3a77c-108">stato di visualizzazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="3a77c-108">the link's display state.</span></span> <span data-ttu-id="3a77c-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a77c-109">This can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="3a77c-110">(1)</span><span class="sxs-lookup"><span data-stu-id="3a77c-110">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3a77c-111">Attiva e visualizza una finestra.</span><span class="sxs-lookup"><span data-stu-id="3a77c-111">Activates and displays a window.</span></span> <span data-ttu-id="3a77c-112">Se la finestra è ridotta a icona o ingrandita, il sistema ripristina le dimensioni e la posizione originali.</span><span class="sxs-lookup"><span data-stu-id="3a77c-112">If the window is minimized or maximized, the system restores it to its original size and position.</span></span>

</dd> <dt>



 <span data-ttu-id="3a77c-113">(2)</span><span class="sxs-lookup"><span data-stu-id="3a77c-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="3a77c-114">Attiva la finestra e la Visualizza come finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="3a77c-114">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>



 <span data-ttu-id="3a77c-115">(3)</span><span class="sxs-lookup"><span data-stu-id="3a77c-115">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3a77c-116">Attiva la finestra e la Visualizza come finestra ingrandita.</span><span class="sxs-lookup"><span data-stu-id="3a77c-116">Activates the window and displays it as a maximized window.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3a77c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a77c-117">Examples</span></span>

<span data-ttu-id="3a77c-118">Nell'esempio seguente viene illustrato l'utilizzo corretto di questa proprietà in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3a77c-118">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3a77c-119">JScript</span><span class="sxs-lookup"><span data-stu-id="3a77c-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



<span data-ttu-id="3a77c-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="3a77c-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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



<span data-ttu-id="3a77c-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3a77c-121">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3a77c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a77c-122">Requirements</span></span>



| <span data-ttu-id="3a77c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a77c-123">Requirement</span></span> | <span data-ttu-id="3a77c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3a77c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a77c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a77c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a77c-126">Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="3a77c-126">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a77c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a77c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a77c-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a77c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3a77c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a77c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a77c-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a77c-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3a77c-131">IDL</span><span class="sxs-lookup"><span data-stu-id="3a77c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a77c-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a77c-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3a77c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3a77c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a77c-134"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3a77c-134"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




