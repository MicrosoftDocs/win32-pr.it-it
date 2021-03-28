---
description: Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona Mostra finestre affiancate.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Metodo IShellDispatch. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978079"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="7fdc1-104">IShellDispatch. TileVertically, metodo</span><span class="sxs-lookup"><span data-stu-id="7fdc1-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="7fdc1-105">Riquadri verticalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="7fdc1-106">Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona **Mostra finestre affiancate**.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fdc1-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="7fdc1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fdc1-108">Parameters</span></span>

<span data-ttu-id="7fdc1-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fdc1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fdc1-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7fdc1-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7fdc1-111">JScript</span></span>

<span data-ttu-id="7fdc1-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7fdc1-113">VB</span><span class="sxs-lookup"><span data-stu-id="7fdc1-113">VB</span></span>

<span data-ttu-id="7fdc1-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fdc1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fdc1-115">Remarks</span></span>

<span data-ttu-id="7fdc1-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. TileVertically**](shell-tilevertically.md) .</span><span class="sxs-lookup"><span data-stu-id="7fdc1-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7fdc1-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="7fdc1-117">Examples</span></span>

<span data-ttu-id="7fdc1-118">Negli esempi seguenti viene illustrato l'utilizzo di **TileVertically** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7fdc1-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7fdc1-119">JScript</span><span class="sxs-lookup"><span data-stu-id="7fdc1-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="7fdc1-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="7fdc1-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7fdc1-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7fdc1-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7fdc1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fdc1-122">Requirements</span></span>



| <span data-ttu-id="7fdc1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fdc1-123">Requirement</span></span> | <span data-ttu-id="7fdc1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7fdc1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdc1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fdc1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7fdc1-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7fdc1-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7fdc1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fdc1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7fdc1-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fdc1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7fdc1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fdc1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fdc1-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fdc1-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7fdc1-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7fdc1-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fdc1-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fdc1-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7fdc1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7fdc1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fdc1-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7fdc1-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




