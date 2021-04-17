---
description: Sincronizza tutti i file offline nella cartella.
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Metodo Cartella2. Synchronize (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401524"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="4cf00-103">Metodo Cartella2. Synchronize</span><span class="sxs-lookup"><span data-stu-id="4cf00-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="4cf00-104">Sincronizza tutti i file offline nella cartella.</span><span class="sxs-lookup"><span data-stu-id="4cf00-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cf00-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="4cf00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cf00-106">Parameters</span></span>

<span data-ttu-id="4cf00-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4cf00-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf00-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cf00-108">Remarks</span></span>

<span data-ttu-id="4cf00-109">Per usare questo metodo, è necessario abilitare la funzionalità File offline.</span><span class="sxs-lookup"><span data-stu-id="4cf00-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="4cf00-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="4cf00-110">Examples</span></span>

<span data-ttu-id="4cf00-111">Nell'esempio seguente viene illustrato l'utilizzo corretto di **Synchronize** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4cf00-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4cf00-112">JScript</span><span class="sxs-lookup"><span data-stu-id="4cf00-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="4cf00-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="4cf00-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="4cf00-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4cf00-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4cf00-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cf00-115">Requirements</span></span>



| <span data-ttu-id="4cf00-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf00-116">Requirement</span></span> | <span data-ttu-id="4cf00-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4cf00-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf00-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cf00-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf00-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4cf00-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cf00-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cf00-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf00-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cf00-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4cf00-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cf00-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf00-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf00-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4cf00-124">IDL</span><span class="sxs-lookup"><span data-stu-id="4cf00-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cf00-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cf00-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4cf00-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf00-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf00-127"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4cf00-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf00-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cf00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf00-129">**Cartella2**</span><span class="sxs-lookup"><span data-stu-id="4cf00-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="4cf00-130">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="4cf00-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




