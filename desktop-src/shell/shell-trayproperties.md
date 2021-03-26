---
description: Consente di visualizzare la barra delle applicazioni e la finestra di dialogo Proprietà menu Start. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Proprietà.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Metodo Shell. TrayProperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980602"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="27a2e-104">Shell. TrayProperties, metodo</span><span class="sxs-lookup"><span data-stu-id="27a2e-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="27a2e-105">Consente di visualizzare la **barra delle applicazioni e la finestra di dialogo Proprietà menu Start** .</span><span class="sxs-lookup"><span data-stu-id="27a2e-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="27a2e-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="27a2e-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a2e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27a2e-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="27a2e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="27a2e-108">Parameters</span></span>

<span data-ttu-id="27a2e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="27a2e-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="27a2e-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="27a2e-110">Examples</span></span>

<span data-ttu-id="27a2e-111">Nell'esempio seguente viene illustrato **TrayProperties** in uso.</span><span class="sxs-lookup"><span data-stu-id="27a2e-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="27a2e-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="27a2e-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="27a2e-113">JScript</span><span class="sxs-lookup"><span data-stu-id="27a2e-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="27a2e-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="27a2e-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="27a2e-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="27a2e-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="27a2e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27a2e-116">Requirements</span></span>



| <span data-ttu-id="27a2e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27a2e-117">Requirement</span></span> | <span data-ttu-id="27a2e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="27a2e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a2e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27a2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27a2e-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="27a2e-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27a2e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27a2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27a2e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27a2e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27a2e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27a2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="27a2e-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="27a2e-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="27a2e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="27a2e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27a2e-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27a2e-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="27a2e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="27a2e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27a2e-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="27a2e-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




