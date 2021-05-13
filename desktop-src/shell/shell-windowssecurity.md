---
description: 'Metodo Shell.WindowsSecurity: visualizza la Sicurezza di Windows di dialogo.'
title: Metodo Shell.WindowsSecurity (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: 2c6e18ba2388909390b856deb03b65b078f810d9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840862"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="97a36-103">Metodo Shell.WindowsSecurity</span><span class="sxs-lookup"><span data-stu-id="97a36-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="97a36-104">Consente di visualizzare **Sicurezza di Windows** finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="97a36-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97a36-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="97a36-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97a36-106">Parameters</span></span>

<span data-ttu-id="97a36-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="97a36-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97a36-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97a36-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="97a36-109">JScript</span><span class="sxs-lookup"><span data-stu-id="97a36-109">JScript</span></span>

<span data-ttu-id="97a36-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="97a36-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="97a36-111">VB</span><span class="sxs-lookup"><span data-stu-id="97a36-111">VB</span></span>

<span data-ttu-id="97a36-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="97a36-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a36-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="97a36-113">Remarks</span></span>

<span data-ttu-id="97a36-114">Questo metodo visualizza la finestra di dialogo visualizzata dopo aver premuto CTRL+ALT+CANC o usando l'opzione di sicurezza nel menu **Start.**</span><span class="sxs-lookup"><span data-stu-id="97a36-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="97a36-115">Questo metodo può essere usato solo quando è connesso da una sessione terminal a Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="97a36-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="97a36-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="97a36-116">Examples</span></span>

<span data-ttu-id="97a36-117">Gli esempi seguenti illustrano l'uso di **WindowsSecurity** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97a36-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="97a36-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="97a36-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="97a36-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="97a36-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="97a36-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="97a36-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="97a36-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97a36-121">Requirements</span></span>



| <span data-ttu-id="97a36-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97a36-122">Requirement</span></span> | <span data-ttu-id="97a36-123">Valore</span><span class="sxs-lookup"><span data-stu-id="97a36-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a36-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97a36-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97a36-125">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="97a36-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="97a36-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97a36-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97a36-127">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="97a36-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="97a36-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97a36-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97a36-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="97a36-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="97a36-130">Idl</span><span class="sxs-lookup"><span data-stu-id="97a36-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97a36-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="97a36-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="97a36-132">DLL</span><span class="sxs-lookup"><span data-stu-id="97a36-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97a36-133"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="97a36-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




