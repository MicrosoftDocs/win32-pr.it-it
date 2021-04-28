---
description: 'Metodo Shell.Open: apre la cartella specificata.'
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Metodo Shell.Open (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 36f8914be3fce6b461e5267562e6f3ef40aa5fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104229"
---
# <a name="shellopen-method"></a><span data-ttu-id="0b097-103">Metodo Shell.Open</span><span class="sxs-lookup"><span data-stu-id="0b097-103">Shell.Open method</span></span>

<span data-ttu-id="0b097-104">Apre la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="0b097-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b097-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b097-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="0b097-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b097-107">*vDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0b097-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b097-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="0b097-108">Type: **Variant**</span></span>

<span data-ttu-id="0b097-109">Stringa che specifica il percorso della cartella o uno dei [**valori ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="0b097-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="0b097-110">Si noti che i nomi delle costanti presenti in **ShellSpecialFolderConstants** sono disponibili in Visual Basic, ma non in VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="0b097-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="0b097-111">In questi casi, i valori numerici devono essere usati al loro posto.</span><span class="sxs-lookup"><span data-stu-id="0b097-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="0b097-112">Se *vDir* è impostato su uno di [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) e la cartella speciale non esiste, questa funzione creerà la cartella.</span><span class="sxs-lookup"><span data-stu-id="0b097-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0b097-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b097-113">Examples</span></span>

<span data-ttu-id="0b097-114">L'esempio seguente illustra **Open** in uso.</span><span class="sxs-lookup"><span data-stu-id="0b097-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="0b097-115">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0b097-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0b097-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="0b097-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="0b097-117">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="0b097-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0b097-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0b097-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0b097-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b097-119">Requirements</span></span>



| <span data-ttu-id="0b097-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b097-120">Requirement</span></span> | <span data-ttu-id="0b097-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0b097-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b097-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b097-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b097-123">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0b097-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0b097-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b097-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b097-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b097-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b097-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b097-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b097-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="0b097-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0b097-128">Idl</span><span class="sxs-lookup"><span data-stu-id="0b097-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b097-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b097-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0b097-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0b097-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b097-131"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0b097-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b097-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b097-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b097-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="0b097-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="0b097-134">**Esplora**</span><span class="sxs-lookup"><span data-stu-id="0b097-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




