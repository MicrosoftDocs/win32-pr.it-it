---
description: Crea una nuova cartella.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Metodo Folder. NewFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967451"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="2be84-103">Folder. NewFolder, metodo</span><span class="sxs-lookup"><span data-stu-id="2be84-103">Folder.NewFolder method</span></span>

<span data-ttu-id="2be84-104">Crea una nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="2be84-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2be84-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="2be84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2be84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be84-107">*bnome*</span><span class="sxs-lookup"><span data-stu-id="2be84-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="2be84-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2be84-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2be84-109">Stringa che specifica il nome della nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="2be84-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="2be84-110">*vOptions* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="2be84-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2be84-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="2be84-111">Type: **Variant**</span></span>

<span data-ttu-id="2be84-112">Questo valore non è attualmente usato.</span><span class="sxs-lookup"><span data-stu-id="2be84-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be84-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2be84-113">Return value</span></span>

<span data-ttu-id="2be84-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2be84-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2be84-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2be84-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2be84-116">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="2be84-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="2be84-117">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="2be84-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="2be84-118">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="2be84-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2be84-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="2be84-119">Examples</span></span>

<span data-ttu-id="2be84-120">Nell'esempio seguente viene usato **NewFolder** per creare la nuova cartella C: \\ TestFolder.</span><span class="sxs-lookup"><span data-stu-id="2be84-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="2be84-121">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2be84-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2be84-122">JScript</span><span class="sxs-lookup"><span data-stu-id="2be84-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="2be84-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="2be84-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2be84-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2be84-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2be84-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2be84-125">Requirements</span></span>



| <span data-ttu-id="2be84-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be84-126">Requirement</span></span> | <span data-ttu-id="2be84-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2be84-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be84-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2be84-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2be84-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2be84-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2be84-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2be84-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2be84-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2be84-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2be84-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2be84-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2be84-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be84-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2be84-134">IDL</span><span class="sxs-lookup"><span data-stu-id="2be84-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2be84-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2be84-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2be84-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2be84-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be84-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2be84-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
