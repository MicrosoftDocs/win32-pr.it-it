---
description: Recupera l'oggetto FolderItem per un elemento specificato nella raccolta.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: Metodo FolderItems. Item (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977039"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="119a2-103">Metodo FolderItems. Item</span><span class="sxs-lookup"><span data-stu-id="119a2-103">FolderItems.Item method</span></span>

<span data-ttu-id="119a2-104">Recupera l'oggetto [**FolderItem**](folderitem.md) per un elemento specificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="119a2-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="119a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="119a2-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="119a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="119a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="119a2-107">*iIndex* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="119a2-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="119a2-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="119a2-108">Type: **Variant**</span></span>

<span data-ttu-id="119a2-109">Indice in base zero dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="119a2-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="119a2-110">Questo valore deve essere minore del valore della proprietà [**count**](folderitems-count.md) .</span><span class="sxs-lookup"><span data-stu-id="119a2-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119a2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="119a2-111">Return value</span></span>

<span data-ttu-id="119a2-112">Riferimento all'oggetto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="119a2-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="119a2-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="119a2-113">Examples</span></span>

<span data-ttu-id="119a2-114">Nell'esempio seguente viene usato **Item** per recuperare l'oggetto [**FolderItem**](folderitem.md) che rappresenta il file di Notepad.exe trovato nella cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="119a2-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="119a2-115">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="119a2-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="119a2-116">JScript</span><span class="sxs-lookup"><span data-stu-id="119a2-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="119a2-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="119a2-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
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
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="119a2-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="119a2-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
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
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="119a2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="119a2-119">Requirements</span></span>



| <span data-ttu-id="119a2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="119a2-120">Requirement</span></span> | <span data-ttu-id="119a2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="119a2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="119a2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="119a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="119a2-123">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="119a2-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="119a2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="119a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="119a2-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="119a2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="119a2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="119a2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="119a2-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="119a2-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="119a2-128">IDL</span><span class="sxs-lookup"><span data-stu-id="119a2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="119a2-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="119a2-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="119a2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="119a2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="119a2-131"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="119a2-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119a2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="119a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119a2-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="119a2-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




