---
description: Restituisce un valore che indica se un particolare servizio è in esecuzione.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Metodo Shell. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881906"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="4960d-103">Shell. IsServiceRunning, metodo</span><span class="sxs-lookup"><span data-stu-id="4960d-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="4960d-104">Restituisce un valore che indica se un particolare servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4960d-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="4960d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4960d-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="4960d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4960d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4960d-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4960d-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4960d-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4960d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4960d-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4960d-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4960d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4960d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4960d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4960d-111">JScript</span></span>

<span data-ttu-id="4960d-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="4960d-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="4960d-113">Restituisce _ *true*\* se il servizio specificato da *sServiceName* è in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4960d-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="4960d-114">VB</span><span class="sxs-lookup"><span data-stu-id="4960d-114">VB</span></span>

<span data-ttu-id="4960d-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="4960d-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="4960d-116">Restituisce _ *true*\* se il servizio specificato da *sServiceName* è in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4960d-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4960d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4960d-117">Remarks</span></span>

<span data-ttu-id="4960d-118">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4960d-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="4960d-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="4960d-119">Examples</span></span>

<span data-ttu-id="4960d-120">Negli esempi seguenti viene illustrato l'utilizzo di **IsServiceRunning** per determinare se il servizio temi è in esecuzione per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4960d-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="4960d-121">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="4960d-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="4960d-122">JScript</span><span class="sxs-lookup"><span data-stu-id="4960d-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="4960d-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="4960d-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="4960d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4960d-124">Requirements</span></span>



| <span data-ttu-id="4960d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4960d-125">Requirement</span></span> | <span data-ttu-id="4960d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4960d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4960d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4960d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4960d-128">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4960d-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4960d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4960d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4960d-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4960d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4960d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4960d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4960d-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4960d-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4960d-133">IDL</span><span class="sxs-lookup"><span data-stu-id="4960d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4960d-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4960d-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4960d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4960d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4960d-136"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4960d-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
