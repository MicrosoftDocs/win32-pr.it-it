---
description: Recupera un oggetto FolderItems che rappresenta la raccolta di elementi nella cartella.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Metodo Folder. Items (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345406"
---
# <a name="folderitems-method"></a><span data-ttu-id="94434-103">Folder. Items (metodo)</span><span class="sxs-lookup"><span data-stu-id="94434-103">Folder.Items method</span></span>

<span data-ttu-id="94434-104">Recupera un oggetto [**FolderItems**](folderitems.md) che rappresenta la raccolta di elementi nella cartella.</span><span class="sxs-lookup"><span data-stu-id="94434-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="94434-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94434-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="94434-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94434-106">Parameters</span></span>

<span data-ttu-id="94434-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="94434-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94434-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94434-108">Return value</span></span>

<span data-ttu-id="94434-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="94434-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="94434-110">Riferimento all'oggetto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="94434-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="94434-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94434-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94434-112">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="94434-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="94434-113">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="94434-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="94434-114">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="94434-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="94434-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="94434-115">Examples</span></span>

<span data-ttu-id="94434-116">Nell'esempio seguente vengono usati **gli elementi** per determinare il numero di elementi nella cartella C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="94434-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="94434-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="94434-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="94434-118">JScript</span><span class="sxs-lookup"><span data-stu-id="94434-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="94434-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="94434-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="94434-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="94434-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="94434-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94434-121">Requirements</span></span>



| <span data-ttu-id="94434-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="94434-122">Requirement</span></span> | <span data-ttu-id="94434-123">Valore</span><span class="sxs-lookup"><span data-stu-id="94434-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94434-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94434-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94434-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94434-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94434-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94434-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94434-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94434-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94434-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94434-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="94434-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94434-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="94434-130">IDL</span><span class="sxs-lookup"><span data-stu-id="94434-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94434-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94434-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="94434-132">DLL</span><span class="sxs-lookup"><span data-stu-id="94434-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94434-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="94434-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




