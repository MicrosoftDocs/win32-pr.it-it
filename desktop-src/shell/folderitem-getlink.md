---
description: Contiene l'oggetto ShellLinkObject dell'elemento, se l'elemento è un tasto di scelta rapida.
ms.assetid: 6444476a-a065-4f69-9330-584e30dbe30d
title: Proprietà FolderItem. GetLink (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d12c0fbd296610174c8b8363602288f59fcb9714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127851"
---
# <a name="folderitemgetlink-property"></a><span data-ttu-id="57316-103">Proprietà FolderItem. GetLink</span><span class="sxs-lookup"><span data-stu-id="57316-103">FolderItem.GetLink property</span></span>

<span data-ttu-id="57316-104">Contiene l'oggetto [**ShellLinkObject**](shelllinkobject-object.md) dell'elemento, se l'elemento è un tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="57316-104">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span>

<span data-ttu-id="57316-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57316-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57316-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57316-106">Syntax</span></span>


```JScript
objGetLink = FolderItem.GetLink
```



## <a name="property-value"></a><span data-ttu-id="57316-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="57316-107">Property value</span></span>

<span data-ttu-id="57316-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto [**ShellLinkObject**](shelllinkobject-object.md) .</span><span class="sxs-lookup"><span data-stu-id="57316-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the [**ShellLinkObject**](shelllinkobject-object.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="57316-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="57316-109">Examples</span></span>

<span data-ttu-id="57316-110">Nell'esempio seguente viene usato **GetLink** per recuperare l'oggetto [**ShellLinkObject**](shelllinkobject-object.md) per un collegamento a Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="57316-110">The following example uses **GetLink** to retrieve the [**ShellLinkObject**](shelllinkobject-object.md) object for a shortcut to Internet Explorer.</span></span> <span data-ttu-id="57316-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="57316-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="57316-112">JScript</span><span class="sxs-lookup"><span data-stu-id="57316-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objLink;
                
                objLink = objFolderItem.GetLink;
                if (objLink != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="57316-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="57316-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetLinkVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objLink
                                
                    set objLink = objFolderItem.GetLink
                    if (not objLink is nothing) then
                        'Add code here          
                    end if
                    set objLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="57316-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="57316-114">Visual Basic:</span></span>


```VB
Private Sub fnGetLinkVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objLink As ShellLinkObject
                    
                    Set objLink = objFolderItem.GetLink
                        If (Not objLink Is Nothing) Then
                            'Add code here
                        Else
                            'Folder object returned nothing
                        End If
                    Set objLink = Nothing
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



## <a name="requirements"></a><span data-ttu-id="57316-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57316-115">Requirements</span></span>



| <span data-ttu-id="57316-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="57316-116">Requirement</span></span> | <span data-ttu-id="57316-117">Valore</span><span class="sxs-lookup"><span data-stu-id="57316-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57316-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57316-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57316-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="57316-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57316-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57316-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57316-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57316-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57316-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57316-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57316-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57316-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="57316-124">IDL</span><span class="sxs-lookup"><span data-stu-id="57316-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57316-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57316-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="57316-126">DLL</span><span class="sxs-lookup"><span data-stu-id="57316-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57316-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="57316-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57316-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57316-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57316-129">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="57316-129">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="57316-130">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="57316-130">**IsLink**</span></span>](folderitem-islink.md)
</dt> </dl>

 

 
