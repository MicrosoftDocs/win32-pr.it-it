---
description: Apre la cartella specificata.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Metodo IShellDispatch. Open (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753087"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="5a685-103">Metodo IShellDispatch. Open</span><span class="sxs-lookup"><span data-stu-id="5a685-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="5a685-104">Apre la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="5a685-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a685-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a685-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="5a685-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a685-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a685-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a685-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5a685-108">Type: **Variant**</span></span>

<span data-ttu-id="5a685-109">Stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="5a685-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="5a685-110">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="5a685-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="5a685-111">In questi casi, i valori numerici devono essere usati al suo posto.</span><span class="sxs-lookup"><span data-stu-id="5a685-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="5a685-112">Se *vdir* è impostato su uno dei [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e la cartella speciale non esiste, la funzione creerà la cartella.</span><span class="sxs-lookup"><span data-stu-id="5a685-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a685-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a685-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5a685-114">JScript</span><span class="sxs-lookup"><span data-stu-id="5a685-114">JScript</span></span>

<span data-ttu-id="5a685-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5a685-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5a685-116">VB</span><span class="sxs-lookup"><span data-stu-id="5a685-116">VB</span></span>

<span data-ttu-id="5a685-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5a685-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a685-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a685-118">Remarks</span></span>

<span data-ttu-id="5a685-119">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="5a685-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="5a685-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="5a685-120">Examples</span></span>

<span data-ttu-id="5a685-121">Negli esempi seguenti viene illustrato l'utilizzo di **Open** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5a685-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5a685-122">JScript</span><span class="sxs-lookup"><span data-stu-id="5a685-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="5a685-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="5a685-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5a685-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5a685-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5a685-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a685-125">Requirements</span></span>



| <span data-ttu-id="5a685-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a685-126">Requirement</span></span> | <span data-ttu-id="5a685-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5a685-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a685-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a685-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5a685-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a685-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a685-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a685-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5a685-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a685-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a685-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a685-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a685-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a685-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5a685-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5a685-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a685-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a685-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5a685-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5a685-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a685-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5a685-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a685-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a685-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a685-139">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="5a685-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="5a685-140">**Esplora**</span><span class="sxs-lookup"><span data-stu-id="5a685-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




