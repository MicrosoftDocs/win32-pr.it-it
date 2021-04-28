---
description: 'Metodo IShellDispatch4.WindowsSecurity: visualizza la Sicurezza di Windows finestra di dialogo.'
title: Metodo IShellDispatch4.WindowsSecurity (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 2d7e8cfbd1e7a2a2392b78487c6a58b62de6df6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116809"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="4ebc9-103">Metodo IShellDispatch4.WindowsSecurity</span><span class="sxs-lookup"><span data-stu-id="4ebc9-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="4ebc9-104">Consente di visualizzare **Sicurezza di Windows** finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebc9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ebc9-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="4ebc9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ebc9-106">Parameters</span></span>

<span data-ttu-id="4ebc9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ebc9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ebc9-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4ebc9-109">JScript</span><span class="sxs-lookup"><span data-stu-id="4ebc9-109">JScript</span></span>

<span data-ttu-id="4ebc9-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4ebc9-111">VB</span><span class="sxs-lookup"><span data-stu-id="4ebc9-111">VB</span></span>

<span data-ttu-id="4ebc9-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebc9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ebc9-113">Remarks</span></span>

<span data-ttu-id="4ebc9-114">Questo metodo visualizza la finestra di dialogo visualizzata dopo aver premuto CTRL+ALT+CANC o usando l'opzione di sicurezza nel menu **Start.**</span><span class="sxs-lookup"><span data-stu-id="4ebc9-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="4ebc9-115">Questo metodo può essere usato solo quando è connesso da una sessione del terminale a Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4ebc9-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4ebc9-116">Examples</span></span>

<span data-ttu-id="4ebc9-117">Gli esempi seguenti illustrano l'uso di **WindowsSecurity** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4ebc9-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4ebc9-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="4ebc9-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="4ebc9-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="4ebc9-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4ebc9-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4ebc9-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4ebc9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ebc9-121">Requirements</span></span>



| <span data-ttu-id="4ebc9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebc9-122">Requirement</span></span> | <span data-ttu-id="4ebc9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4ebc9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebc9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ebc9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebc9-125">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4ebc9-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4ebc9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ebc9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebc9-127">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ebc9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4ebc9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ebc9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ebc9-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc9-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4ebc9-130">Idl</span><span class="sxs-lookup"><span data-stu-id="4ebc9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ebc9-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc9-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4ebc9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4ebc9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ebc9-133"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc9-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




