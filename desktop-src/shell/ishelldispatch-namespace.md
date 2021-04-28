---
description: 'Metodo IShellDispatch.NameSpace: crea e restituisce un oggetto Folder per la cartella specificata.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Metodo IShellDispatch.NameSpace (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100519"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="b1928-103">Metodo IShellDispatch.NameSpace</span><span class="sxs-lookup"><span data-stu-id="b1928-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="b1928-104">Crea e restituisce un [**oggetto Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b1928-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1928-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1928-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="b1928-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1928-107">*vDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b1928-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1928-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="b1928-108">Type: **Variant**</span></span>

<span data-ttu-id="b1928-109">Cartella per la quale creare [**l'oggetto**](folder.md) Folder.</span><span class="sxs-lookup"><span data-stu-id="b1928-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="b1928-110">Può essere una stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="b1928-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="b1928-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="b1928-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="b1928-112">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="b1928-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1928-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1928-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b1928-114">JScript</span><span class="sxs-lookup"><span data-stu-id="b1928-114">JScript</span></span>

<span data-ttu-id="b1928-115">Tipo: **[ **Cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1928-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="b1928-116">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b1928-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="b1928-117">Se la cartella non viene creata correttamente, questo valore restituisce **null.**</span><span class="sxs-lookup"><span data-stu-id="b1928-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="b1928-118">VB</span><span class="sxs-lookup"><span data-stu-id="b1928-118">VB</span></span>

<span data-ttu-id="b1928-119">Tipo: **[ **Cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1928-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="b1928-120">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b1928-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="b1928-121">Se la cartella non viene creata correttamente, questo valore restituisce **null.**</span><span class="sxs-lookup"><span data-stu-id="b1928-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1928-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1928-122">Remarks</span></span>

<span data-ttu-id="b1928-123">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.NameSpace.**](shell-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1928-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b1928-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1928-124">Examples</span></span>

<span data-ttu-id="b1928-125">Gli esempi seguenti illustrano l'uso [**di NameSpace**](shell-namespace.md) in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b1928-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b1928-126">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b1928-126">JScript:</span></span>


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



<span data-ttu-id="b1928-127">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b1928-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b1928-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b1928-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b1928-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1928-129">Requirements</span></span>



| <span data-ttu-id="b1928-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1928-130">Requirement</span></span> | <span data-ttu-id="b1928-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b1928-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1928-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1928-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1928-133">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b1928-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b1928-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1928-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1928-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1928-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1928-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1928-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1928-137"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1928-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b1928-138">Idl</span><span class="sxs-lookup"><span data-stu-id="b1928-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1928-139"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1928-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b1928-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b1928-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1928-141"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b1928-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




