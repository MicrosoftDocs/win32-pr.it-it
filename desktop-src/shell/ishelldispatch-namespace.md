---
description: Crea e restituisce un oggetto Folder per la cartella specificata.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Metodo IShellDispatch. NameSpace (shldisp. h)
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
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527343"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="b3cbf-103">IShellDispatch. NameSpace, metodo</span><span class="sxs-lookup"><span data-stu-id="b3cbf-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="b3cbf-104">Crea e restituisce un oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cbf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3cbf-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b3cbf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3cbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3cbf-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3cbf-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3cbf-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-108">Type: **Variant**</span></span>

<span data-ttu-id="b3cbf-109">Cartella per cui creare l'oggetto [**cartella**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="b3cbf-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="b3cbf-110">Può trattarsi di una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="b3cbf-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="b3cbf-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="b3cbf-112">In questi casi, i valori numerici devono essere usati al suo posto.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3cbf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3cbf-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b3cbf-114">JScript</span><span class="sxs-lookup"><span data-stu-id="b3cbf-114">JScript</span></span>

<span data-ttu-id="b3cbf-115">Tipo: **[ **cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3cbf-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="b3cbf-116">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="b3cbf-117">Se la cartella non viene creata correttamente, questo valore restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="b3cbf-118">VB</span><span class="sxs-lookup"><span data-stu-id="b3cbf-118">VB</span></span>

<span data-ttu-id="b3cbf-119">Tipo: **[ **cartella**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3cbf-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="b3cbf-120">Riferimento all'oggetto [**Folder**](folder.md) per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="b3cbf-121">Se la cartella non viene creata correttamente, questo valore restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cbf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3cbf-122">Remarks</span></span>

<span data-ttu-id="b3cbf-123">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="b3cbf-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b3cbf-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3cbf-124">Examples</span></span>

<span data-ttu-id="b3cbf-125">Negli esempi seguenti viene illustrato l'utilizzo dello [**spazio dei nomi**](shell-namespace.md) in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b3cbf-126">JScript</span><span class="sxs-lookup"><span data-stu-id="b3cbf-126">JScript:</span></span>


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



<span data-ttu-id="b3cbf-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="b3cbf-127">VBScript:</span></span>


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



<span data-ttu-id="b3cbf-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b3cbf-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b3cbf-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3cbf-129">Requirements</span></span>



| <span data-ttu-id="b3cbf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cbf-130">Requirement</span></span> | <span data-ttu-id="b3cbf-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b3cbf-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cbf-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cbf-133">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3cbf-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3cbf-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cbf-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3cbf-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3cbf-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3cbf-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3cbf-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbf-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b3cbf-138">IDL</span><span class="sxs-lookup"><span data-stu-id="b3cbf-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3cbf-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbf-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b3cbf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b3cbf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3cbf-141"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbf-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




