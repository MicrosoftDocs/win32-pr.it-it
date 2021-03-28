---
description: Apre una cartella specificata in una finestra di Esplora risorse.
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Metodo IShellDispatch. explore (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1ae29b4962dcac1be0b7ea23808e36ce005cb62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978114"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="eac8e-103">Metodo IShellDispatch. explore</span><span class="sxs-lookup"><span data-stu-id="eac8e-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="eac8e-104">Apre una cartella specificata in una finestra di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="eac8e-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eac8e-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="eac8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eac8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac8e-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eac8e-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eac8e-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="eac8e-108">Type: **Variant**</span></span>

<span data-ttu-id="eac8e-109">Cartella da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="eac8e-109">The folder to be displayed.</span></span> <span data-ttu-id="eac8e-110">Può trattarsi di una stringa che specifica il percorso della cartella o uno dei valori [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="eac8e-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="eac8e-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="eac8e-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="eac8e-112">In questi casi, i valori numerici devono essere usati al suo posto.</span><span class="sxs-lookup"><span data-stu-id="eac8e-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac8e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eac8e-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="eac8e-114">JScript</span><span class="sxs-lookup"><span data-stu-id="eac8e-114">JScript</span></span>

<span data-ttu-id="eac8e-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="eac8e-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="eac8e-116">VB</span><span class="sxs-lookup"><span data-stu-id="eac8e-116">VB</span></span>

<span data-ttu-id="eac8e-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="eac8e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac8e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eac8e-118">Remarks</span></span>

<span data-ttu-id="eac8e-119">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. explore**](shell-explore.md) .</span><span class="sxs-lookup"><span data-stu-id="eac8e-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="eac8e-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="eac8e-120">Examples</span></span>

<span data-ttu-id="eac8e-121">Negli esempi seguenti viene illustrato l'utilizzo di **Esplora** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="eac8e-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="eac8e-122">JScript</span><span class="sxs-lookup"><span data-stu-id="eac8e-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="eac8e-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="eac8e-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="eac8e-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="eac8e-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="eac8e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eac8e-125">Requirements</span></span>



| <span data-ttu-id="eac8e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac8e-126">Requirement</span></span> | <span data-ttu-id="eac8e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="eac8e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac8e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac8e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eac8e-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eac8e-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eac8e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac8e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eac8e-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eac8e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eac8e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eac8e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac8e-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac8e-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="eac8e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="eac8e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eac8e-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eac8e-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="eac8e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eac8e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eac8e-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="eac8e-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




