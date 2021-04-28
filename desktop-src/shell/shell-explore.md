---
description: 'Metodo Shell.Explore: apre una cartella specificata in una Esplora risorse finestra.'
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Metodo Shell.Explore (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104329"
---
# <a name="shellexplore-method"></a><span data-ttu-id="63781-103">Metodo Shell.Explore</span><span class="sxs-lookup"><span data-stu-id="63781-103">Shell.Explore method</span></span>

<span data-ttu-id="63781-104">Apre una cartella specificata in una finestra Esplora risorse dati.</span><span class="sxs-lookup"><span data-stu-id="63781-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="63781-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63781-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="63781-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63781-107">*vDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="63781-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63781-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="63781-108">Type: **Variant**</span></span>

<span data-ttu-id="63781-109">Cartella da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="63781-109">The folder to be displayed.</span></span> <span data-ttu-id="63781-110">Può essere una stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="63781-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="63781-111">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="63781-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="63781-112">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="63781-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63781-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63781-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="63781-114">JScript</span><span class="sxs-lookup"><span data-stu-id="63781-114">JScript</span></span>

<span data-ttu-id="63781-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="63781-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="63781-116">VB</span><span class="sxs-lookup"><span data-stu-id="63781-116">VB</span></span>

<span data-ttu-id="63781-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="63781-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="63781-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="63781-118">Examples</span></span>

<span data-ttu-id="63781-119">L'esempio seguente illustra **Esplora** in uso.</span><span class="sxs-lookup"><span data-stu-id="63781-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="63781-120">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="63781-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="63781-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="63781-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="63781-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="63781-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="63781-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="63781-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="63781-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63781-124">Requirements</span></span>



| <span data-ttu-id="63781-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63781-125">Requirement</span></span> | <span data-ttu-id="63781-126">Valore</span><span class="sxs-lookup"><span data-stu-id="63781-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63781-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63781-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63781-128">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="63781-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="63781-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63781-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63781-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63781-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63781-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63781-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="63781-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="63781-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="63781-133">Idl</span><span class="sxs-lookup"><span data-stu-id="63781-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63781-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="63781-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="63781-135">DLL</span><span class="sxs-lookup"><span data-stu-id="63781-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63781-136"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="63781-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




