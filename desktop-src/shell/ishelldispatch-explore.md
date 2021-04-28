---
description: 'Metodo IShellDispatch.Explore: apre una cartella specificata in una Esplora risorse finestra.'
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Metodo IShellDispatch.Explore (Shldisp.h)
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
ms.openlocfilehash: e693985cf7d8d83bd5a00595c42cd4427b0ebd5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100559"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="2b63c-103">Metodo IShellDispatch.Explore</span><span class="sxs-lookup"><span data-stu-id="2b63c-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="2b63c-104">Apre una cartella specificata in una finestra Esplora risorse dati.</span><span class="sxs-lookup"><span data-stu-id="2b63c-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b63c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b63c-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="2b63c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b63c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b63c-107">*vDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2b63c-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b63c-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="2b63c-108">Type: **Variant**</span></span>

<span data-ttu-id="2b63c-109">Cartella da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="2b63c-109">The folder to be displayed.</span></span> <span data-ttu-id="2b63c-110">Può essere una stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="2b63c-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="2b63c-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="2b63c-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="2b63c-112">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="2b63c-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b63c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b63c-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2b63c-114">JScript</span><span class="sxs-lookup"><span data-stu-id="2b63c-114">JScript</span></span>

<span data-ttu-id="2b63c-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2b63c-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2b63c-116">VB</span><span class="sxs-lookup"><span data-stu-id="2b63c-116">VB</span></span>

<span data-ttu-id="2b63c-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2b63c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b63c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b63c-118">Remarks</span></span>

<span data-ttu-id="2b63c-119">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.Explore.**](shell-explore.md)</span><span class="sxs-lookup"><span data-stu-id="2b63c-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2b63c-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b63c-120">Examples</span></span>

<span data-ttu-id="2b63c-121">Gli esempi seguenti illustrano l'uso **di Esplora** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b63c-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2b63c-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="2b63c-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="2b63c-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="2b63c-123">VBScript:</span></span>


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



<span data-ttu-id="2b63c-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2b63c-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2b63c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b63c-125">Requirements</span></span>



| <span data-ttu-id="2b63c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b63c-126">Requirement</span></span> | <span data-ttu-id="2b63c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2b63c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b63c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b63c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2b63c-129">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2b63c-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2b63c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b63c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2b63c-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b63c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b63c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b63c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b63c-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b63c-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2b63c-134">Idl</span><span class="sxs-lookup"><span data-stu-id="2b63c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b63c-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b63c-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2b63c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b63c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b63c-137"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2b63c-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




