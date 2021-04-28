---
description: "Metodo IShellDispatch2.CanStartStopService: determina se l'utente corrente può avviare e arrestare il servizio denominato."
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Metodo IShellDispatch2.CanStartStopService (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117129"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="db9cb-103">Metodo IShellDispatch2.CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="db9cb-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="db9cb-104">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="db9cb-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db9cb-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="db9cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db9cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9cb-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9cb-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="db9cb-108">Type: **String**</span></span>

<span data-ttu-id="db9cb-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="db9cb-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9cb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db9cb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="db9cb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="db9cb-111">JScript</span></span>

<span data-ttu-id="db9cb-112">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="db9cb-112">Type: **Variant\***</span></span>

<span data-ttu-id="db9cb-113">Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="db9cb-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="db9cb-114">VB</span><span class="sxs-lookup"><span data-stu-id="db9cb-114">VB</span></span>

<span data-ttu-id="db9cb-115">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="db9cb-115">Type: **Variant\***</span></span>

<span data-ttu-id="db9cb-116">Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="db9cb-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9cb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="db9cb-117">Remarks</span></span>

<span data-ttu-id="db9cb-118">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.CanStartStopService.**](./shell-canstartstopservice.md)</span><span class="sxs-lookup"><span data-stu-id="db9cb-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="db9cb-119">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="db9cb-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="db9cb-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="db9cb-120">Examples</span></span>

<span data-ttu-id="db9cb-121">Negli esempi seguenti viene illustrato l'utilizzo **di CanStartStopService** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="db9cb-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="db9cb-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="db9cb-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="db9cb-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="db9cb-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="db9cb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db9cb-124">Requirements</span></span>



| <span data-ttu-id="db9cb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9cb-125">Requirement</span></span> | <span data-ttu-id="db9cb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="db9cb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9cb-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9cb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="db9cb-128">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db9cb-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db9cb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="db9cb-130">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db9cb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="db9cb-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db9cb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9cb-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="db9cb-133">Idl</span><span class="sxs-lookup"><span data-stu-id="db9cb-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db9cb-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="db9cb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="db9cb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9cb-136"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="db9cb-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
