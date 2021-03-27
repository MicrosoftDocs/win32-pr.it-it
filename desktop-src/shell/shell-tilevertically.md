---
description: Riquadri verticalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona finestre affiancate verticalmente
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Metodo Shell. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980607"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="2121e-104">Shell. TileVertically, metodo</span><span class="sxs-lookup"><span data-stu-id="2121e-104">Shell.TileVertically method</span></span>

<span data-ttu-id="2121e-105">Riquadri verticalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="2121e-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="2121e-106">Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona **finestre affiancate verticalmente**</span><span class="sxs-lookup"><span data-stu-id="2121e-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2121e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2121e-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="2121e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2121e-108">Parameters</span></span>

<span data-ttu-id="2121e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2121e-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="2121e-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="2121e-110">Examples</span></span>

<span data-ttu-id="2121e-111">Nell'esempio seguente viene illustrato **TileVertically** in uso.</span><span class="sxs-lookup"><span data-stu-id="2121e-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="2121e-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2121e-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2121e-113">JScript</span><span class="sxs-lookup"><span data-stu-id="2121e-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="2121e-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="2121e-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2121e-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2121e-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2121e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2121e-116">Requirements</span></span>



| <span data-ttu-id="2121e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2121e-117">Requirement</span></span> | <span data-ttu-id="2121e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2121e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2121e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2121e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2121e-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2121e-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2121e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2121e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2121e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2121e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2121e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2121e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2121e-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2121e-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2121e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="2121e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2121e-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2121e-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2121e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2121e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2121e-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2121e-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




