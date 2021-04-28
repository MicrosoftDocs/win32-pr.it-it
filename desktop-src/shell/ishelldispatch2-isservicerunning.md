---
description: 'Metodo IShellDispatch2.IsServiceRunning: restituisce un valore che indica se un determinato servizio è in esecuzione.'
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Metodo IShellDispatch2.IsServiceRunning (Shldisp.h)
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
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117089"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="b3e8a-103">Metodo IShellDispatch2.IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="b3e8a-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="b3e8a-104">Restituisce un valore che indica se un determinato servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3e8a-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b3e8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3e8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e8a-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b3e8a-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e8a-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b3e8a-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e8a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3e8a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b3e8a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b3e8a-111">JScript</span></span>

<span data-ttu-id="b3e8a-112">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-112">Type: **Variant\***</span></span>

<span data-ttu-id="b3e8a-113">Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="b3e8a-114">VB</span><span class="sxs-lookup"><span data-stu-id="b3e8a-114">VB</span></span>

<span data-ttu-id="b3e8a-115">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="b3e8a-115">Type: **Variant\***</span></span>

<span data-ttu-id="b3e8a-116">Restituisce **true** se il servizio specificato da *sServiceName è* in esecuzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3e8a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3e8a-117">Remarks</span></span>

<span data-ttu-id="b3e8a-118">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.IsServiceRunning.**](./shell-isservicerunning.md)</span><span class="sxs-lookup"><span data-stu-id="b3e8a-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="b3e8a-119">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b3e8a-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3e8a-120">Examples</span></span>

<span data-ttu-id="b3e8a-121">Gli esempi seguenti illustrano l'uso di **IsServiceRunning** per determinare se il servizio Temi è in esecuzione per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="b3e8a-122">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="b3e8a-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="b3e8a-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b3e8a-123">JScript:</span></span>


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



<span data-ttu-id="b3e8a-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b3e8a-124">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b3e8a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3e8a-125">Requirements</span></span>



| <span data-ttu-id="b3e8a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e8a-126">Requirement</span></span> | <span data-ttu-id="b3e8a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e8a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e8a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e8a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e8a-129">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b3e8a-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3e8a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e8a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e8a-131">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3e8a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b3e8a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3e8a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3e8a-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e8a-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b3e8a-134">Idl</span><span class="sxs-lookup"><span data-stu-id="b3e8a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3e8a-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3e8a-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b3e8a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b3e8a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3e8a-137"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b3e8a-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
