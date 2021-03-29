---
description: Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare Mostra Windows in pila.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Metodo IShellDispatch. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130091"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="d5f17-104">IShellDispatch. TileHorizontally, metodo</span><span class="sxs-lookup"><span data-stu-id="d5f17-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="d5f17-105">Riquadri orizzontalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="d5f17-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="d5f17-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Mostra Windows in pila**.</span><span class="sxs-lookup"><span data-stu-id="d5f17-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f17-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5f17-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="d5f17-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5f17-108">Parameters</span></span>

<span data-ttu-id="d5f17-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d5f17-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5f17-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5f17-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d5f17-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d5f17-111">JScript</span></span>

<span data-ttu-id="d5f17-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d5f17-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d5f17-113">VB</span><span class="sxs-lookup"><span data-stu-id="d5f17-113">VB</span></span>

<span data-ttu-id="d5f17-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d5f17-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f17-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5f17-115">Remarks</span></span>

<span data-ttu-id="d5f17-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. TileHorizontally**](shell-tilehorizontally.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f17-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d5f17-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d5f17-117">Examples</span></span>

<span data-ttu-id="d5f17-118">Nell'esempio seguente viene illustrato l'utilizzo di **TileHorizontally** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d5f17-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d5f17-119">JScript</span><span class="sxs-lookup"><span data-stu-id="d5f17-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="d5f17-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="d5f17-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d5f17-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d5f17-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d5f17-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5f17-122">Requirements</span></span>



| <span data-ttu-id="d5f17-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f17-123">Requirement</span></span> | <span data-ttu-id="d5f17-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d5f17-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f17-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5f17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f17-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d5f17-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d5f17-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5f17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f17-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5f17-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5f17-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5f17-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f17-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f17-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d5f17-131">IDL</span><span class="sxs-lookup"><span data-stu-id="d5f17-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5f17-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f17-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d5f17-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f17-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f17-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d5f17-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




