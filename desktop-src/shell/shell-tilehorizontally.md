---
description: Riquadri orizzontalmente tutte le finestre sul desktop. Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona finestre affiancate orizzontalmente
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Metodo Shell. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232100"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="c0191-104">Shell. TileHorizontally, metodo</span><span class="sxs-lookup"><span data-stu-id="c0191-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="c0191-105">Riquadri orizzontalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="c0191-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="c0191-106">Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona **finestre affiancate orizzontalmente**</span><span class="sxs-lookup"><span data-stu-id="c0191-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0191-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0191-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="c0191-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0191-108">Parameters</span></span>

<span data-ttu-id="c0191-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c0191-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c0191-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0191-110">Examples</span></span>

<span data-ttu-id="c0191-111">Nell'esempio seguente viene illustrato **TileHorizontally** in uso.</span><span class="sxs-lookup"><span data-stu-id="c0191-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="c0191-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c0191-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c0191-113">JScript</span><span class="sxs-lookup"><span data-stu-id="c0191-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="c0191-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="c0191-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c0191-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c0191-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c0191-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0191-116">Requirements</span></span>



| <span data-ttu-id="c0191-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0191-117">Requirement</span></span> | <span data-ttu-id="c0191-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c0191-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0191-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0191-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0191-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c0191-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c0191-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0191-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0191-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0191-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0191-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0191-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0191-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0191-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c0191-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c0191-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0191-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0191-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c0191-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c0191-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0191-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c0191-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




