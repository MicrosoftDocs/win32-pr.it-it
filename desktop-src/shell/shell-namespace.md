---
description: Crea e restituisce un oggetto Folder per la cartella specificata.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Metodo Shell. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231569"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="9e1ce-103">Shell. NameSpace, metodo</span><span class="sxs-lookup"><span data-stu-id="9e1ce-103">Shell.NameSpace method</span></span>

<span data-ttu-id="9e1ce-104">Crea e restituisce un oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e1ce-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="9e1ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e1ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1ce-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1ce-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9e1ce-108">Type: **Variant**</span></span>

<span data-ttu-id="9e1ce-109">Cartella per cui creare l'oggetto [**cartella**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="9e1ce-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="9e1ce-110">Può trattarsi di una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="9e1ce-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="9e1ce-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="9e1ce-112">In questi casi, i valori numerici devono essere usati al suo posto.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1ce-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e1ce-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9e1ce-114">JScript</span><span class="sxs-lookup"><span data-stu-id="9e1ce-114">JScript</span></span>

<span data-ttu-id="9e1ce-115">Tipo: **[ **cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e1ce-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="9e1ce-116">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="9e1ce-117">Se la cartella non viene creata correttamente, questo valore restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="9e1ce-118">VB</span><span class="sxs-lookup"><span data-stu-id="9e1ce-118">VB</span></span>

<span data-ttu-id="9e1ce-119">Tipo: **[ **cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e1ce-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="9e1ce-120">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="9e1ce-121">Se la cartella non viene creata correttamente, questo valore restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="9e1ce-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e1ce-122">Examples</span></span>

<span data-ttu-id="9e1ce-123">Nell'esempio seguente viene illustrato **lo spazio dei nomi** in uso.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="9e1ce-124">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9e1ce-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9e1ce-125">JScript</span><span class="sxs-lookup"><span data-stu-id="9e1ce-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="9e1ce-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="9e1ce-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9e1ce-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9e1ce-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9e1ce-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e1ce-128">Requirements</span></span>



| <span data-ttu-id="9e1ce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e1ce-129">Requirement</span></span> | <span data-ttu-id="9e1ce-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9e1ce-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1ce-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e1ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1ce-132">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e1ce-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e1ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1ce-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e1ce-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e1ce-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e1ce-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1ce-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1ce-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9e1ce-137">IDL</span><span class="sxs-lookup"><span data-stu-id="9e1ce-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e1ce-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e1ce-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9e1ce-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9e1ce-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1ce-140"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9e1ce-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




