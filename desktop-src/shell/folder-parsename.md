---
description: Crea e restituisce un oggetto FolderItem che rappresenta un elemento specificato.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Metodo Folder. ParseName (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749175"
---
# <a name="folderparsename-method"></a><span data-ttu-id="f610b-103">Folder. ParseName, metodo</span><span class="sxs-lookup"><span data-stu-id="f610b-103">Folder.ParseName method</span></span>

<span data-ttu-id="f610b-104">Crea e restituisce un oggetto [**FolderItem**](folderitem.md) che rappresenta un elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="f610b-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f610b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f610b-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="f610b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f610b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f610b-107">*bnome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f610b-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f610b-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f610b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f610b-109">Stringa che specifica il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f610b-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f610b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f610b-110">Return value</span></span>

<span data-ttu-id="f610b-111">Tipo: **[ **FolderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f610b-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="f610b-112">Riferimento all'oggetto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f610b-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f610b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f610b-113">Remarks</span></span>

<span data-ttu-id="f610b-114">**ParseName** non deve essere usato per cartelle virtuali, ad esempio documenti.</span><span class="sxs-lookup"><span data-stu-id="f610b-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="f610b-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="f610b-115">Examples</span></span>

<span data-ttu-id="f610b-116">Nell'esempio seguente viene usato **ParseName** per creare un oggetto che rappresenta l'elemento della cartella Clock.avi nella \\ cartella C: Windows.</span><span class="sxs-lookup"><span data-stu-id="f610b-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="f610b-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f610b-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f610b-118">JScript</span><span class="sxs-lookup"><span data-stu-id="f610b-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="f610b-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="f610b-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="f610b-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f610b-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f610b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f610b-121">Requirements</span></span>



| <span data-ttu-id="f610b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f610b-122">Requirement</span></span> | <span data-ttu-id="f610b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f610b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f610b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f610b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f610b-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f610b-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f610b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f610b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f610b-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f610b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f610b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f610b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f610b-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f610b-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f610b-130">IDL</span><span class="sxs-lookup"><span data-stu-id="f610b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f610b-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f610b-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f610b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f610b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f610b-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f610b-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
