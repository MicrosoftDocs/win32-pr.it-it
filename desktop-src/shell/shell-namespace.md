---
description: 'Metodo Shell.NameSpace: crea e restituisce un oggetto Folder per la cartella specificata.'
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Metodo Shell.NameSpace (Shldisp.h)
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
ms.openlocfilehash: fab501912c55aaaf6cab832bf76763672e830d33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083709"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="c1a44-103">Metodo Shell.NameSpace</span><span class="sxs-lookup"><span data-stu-id="c1a44-103">Shell.NameSpace method</span></span>

<span data-ttu-id="c1a44-104">Crea e restituisce un [**oggetto Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a44-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a44-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1a44-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="c1a44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1a44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a44-107">*vDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c1a44-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a44-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="c1a44-108">Type: **Variant**</span></span>

<span data-ttu-id="c1a44-109">Cartella per la quale creare [**l'oggetto**](folder.md) Folder.</span><span class="sxs-lookup"><span data-stu-id="c1a44-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="c1a44-110">Può essere una stringa che specifica il percorso della cartella o uno dei valori [**shellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="c1a44-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="c1a44-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="c1a44-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="c1a44-112">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="c1a44-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a44-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1a44-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c1a44-114">JScript</span><span class="sxs-lookup"><span data-stu-id="c1a44-114">JScript</span></span>

<span data-ttu-id="c1a44-115">Tipo: **[ **Cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1a44-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="c1a44-116">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a44-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="c1a44-117">Se la cartella non viene creata correttamente, questo valore restituisce **null.**</span><span class="sxs-lookup"><span data-stu-id="c1a44-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="c1a44-118">VB</span><span class="sxs-lookup"><span data-stu-id="c1a44-118">VB</span></span>

<span data-ttu-id="c1a44-119">Tipo: **[ **Cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1a44-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="c1a44-120">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a44-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="c1a44-121">Se la cartella non viene creata correttamente, questo valore restituisce **null.**</span><span class="sxs-lookup"><span data-stu-id="c1a44-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="c1a44-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1a44-122">Examples</span></span>

<span data-ttu-id="c1a44-123">L'esempio seguente mostra **NameSpace** in uso.</span><span class="sxs-lookup"><span data-stu-id="c1a44-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="c1a44-124">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1a44-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c1a44-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c1a44-125">JScript:</span></span>


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



<span data-ttu-id="c1a44-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="c1a44-126">VBScript:</span></span>


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



<span data-ttu-id="c1a44-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c1a44-127">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c1a44-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1a44-128">Requirements</span></span>



| <span data-ttu-id="c1a44-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1a44-129">Requirement</span></span> | <span data-ttu-id="c1a44-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c1a44-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a44-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1a44-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a44-132">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c1a44-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1a44-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1a44-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a44-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1a44-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1a44-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1a44-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1a44-136"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a44-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c1a44-137">Idl</span><span class="sxs-lookup"><span data-stu-id="c1a44-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1a44-138"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1a44-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c1a44-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c1a44-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1a44-140"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c1a44-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




