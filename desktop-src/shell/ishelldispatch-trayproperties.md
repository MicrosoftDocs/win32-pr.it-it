---
description: Consente di visualizzare la barra delle applicazioni e la finestra di dialogo Proprietà menu Start. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Proprietà.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Metodo IShellDispatch. TrayProperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966880"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="aacc4-104">IShellDispatch. TrayProperties, metodo</span><span class="sxs-lookup"><span data-stu-id="aacc4-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="aacc4-105">Consente di visualizzare la **barra delle applicazioni e la finestra di dialogo Proprietà menu Start** .</span><span class="sxs-lookup"><span data-stu-id="aacc4-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="aacc4-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="aacc4-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacc4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aacc4-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="aacc4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aacc4-108">Parameters</span></span>

<span data-ttu-id="aacc4-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aacc4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aacc4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aacc4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="aacc4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="aacc4-111">JScript</span></span>

<span data-ttu-id="aacc4-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aacc4-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="aacc4-113">VB</span><span class="sxs-lookup"><span data-stu-id="aacc4-113">VB</span></span>

<span data-ttu-id="aacc4-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aacc4-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aacc4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aacc4-115">Remarks</span></span>

<span data-ttu-id="aacc4-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="aacc4-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="aacc4-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="aacc4-117">Examples</span></span>

<span data-ttu-id="aacc4-118">Negli esempi seguenti viene illustrato l'utilizzo di **TrayProperties** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="aacc4-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="aacc4-119">JScript</span><span class="sxs-lookup"><span data-stu-id="aacc4-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="aacc4-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="aacc4-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="aacc4-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="aacc4-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="aacc4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aacc4-122">Requirements</span></span>



| <span data-ttu-id="aacc4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aacc4-123">Requirement</span></span> | <span data-ttu-id="aacc4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="aacc4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aacc4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aacc4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aacc4-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aacc4-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aacc4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aacc4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aacc4-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aacc4-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aacc4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aacc4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aacc4-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aacc4-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="aacc4-131">IDL</span><span class="sxs-lookup"><span data-stu-id="aacc4-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aacc4-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aacc4-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="aacc4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aacc4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aacc4-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="aacc4-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




