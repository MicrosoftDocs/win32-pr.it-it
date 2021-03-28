---
description: Restituisce un valore che indica se un particolare servizio è in esecuzione.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Metodo IShellDispatch2. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978047"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="b8b20-103">IShellDispatch2. IsServiceRunning, metodo</span><span class="sxs-lookup"><span data-stu-id="b8b20-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="b8b20-104">Restituisce un valore che indica se un particolare servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b8b20-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b20-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8b20-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="b8b20-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8b20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b20-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8b20-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b20-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b8b20-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b8b20-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="b8b20-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b20-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8b20-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b8b20-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b8b20-111">JScript</span></span>

<span data-ttu-id="b8b20-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="b8b20-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="b8b20-113">Restituisce _ *true*\* se il servizio specificato da *sServiceName* è in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b8b20-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="b8b20-114">VB</span><span class="sxs-lookup"><span data-stu-id="b8b20-114">VB</span></span>

<span data-ttu-id="b8b20-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="b8b20-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="b8b20-116">Restituisce _ *true*\* se il servizio specificato da *sServiceName* è in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b8b20-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b20-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8b20-117">Remarks</span></span>

<span data-ttu-id="b8b20-118">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. IsServiceRunning**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b20-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="b8b20-119">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b8b20-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b8b20-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8b20-120">Examples</span></span>

<span data-ttu-id="b8b20-121">Negli esempi seguenti viene illustrato l'utilizzo di **IsServiceRunning** per determinare se il servizio temi è in esecuzione per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b8b20-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="b8b20-122">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="b8b20-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="b8b20-123">JScript</span><span class="sxs-lookup"><span data-stu-id="b8b20-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="b8b20-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="b8b20-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="b8b20-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8b20-125">Requirements</span></span>



| <span data-ttu-id="b8b20-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b20-126">Requirement</span></span> | <span data-ttu-id="b8b20-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b8b20-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b20-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8b20-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b20-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b8b20-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8b20-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8b20-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b20-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8b20-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b8b20-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8b20-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b20-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b20-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b8b20-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b8b20-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8b20-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8b20-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b8b20-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b8b20-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b20-137"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b20-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
