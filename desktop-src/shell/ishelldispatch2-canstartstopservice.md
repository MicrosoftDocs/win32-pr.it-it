---
description: Determina se l'utente corrente può avviare e arrestare il servizio denominato.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Metodo IShellDispatch2. CanStartStopService (shldisp. h)
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
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527330"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="1633b-103">IShellDispatch2. CanStartStopService, metodo</span><span class="sxs-lookup"><span data-stu-id="1633b-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="1633b-104">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="1633b-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1633b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1633b-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="1633b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1633b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1633b-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1633b-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1633b-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="1633b-108">Type: **String**</span></span>

<span data-ttu-id="1633b-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="1633b-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1633b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1633b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1633b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1633b-111">JScript</span></span>

<span data-ttu-id="1633b-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="1633b-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="1633b-113">Restituisce _ *true*\* se l'utente è in grado di avviare e arrestare il servizio. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1633b-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="1633b-114">VB</span><span class="sxs-lookup"><span data-stu-id="1633b-114">VB</span></span>

<span data-ttu-id="1633b-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="1633b-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="1633b-116">Restituisce _ *true*\* se l'utente è in grado di avviare e arrestare il servizio. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1633b-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1633b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1633b-117">Remarks</span></span>

<span data-ttu-id="1633b-118">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. CanStartStopService**](./shell-canstartstopservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1633b-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="1633b-119">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1633b-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1633b-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="1633b-120">Examples</span></span>

<span data-ttu-id="1633b-121">Negli esempi seguenti viene illustrato l'utilizzo di **CanStartStopService** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="1633b-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="1633b-122">JScript</span><span class="sxs-lookup"><span data-stu-id="1633b-122">JScript:</span></span>


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



<span data-ttu-id="1633b-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="1633b-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1633b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1633b-124">Requirements</span></span>



| <span data-ttu-id="1633b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1633b-125">Requirement</span></span> | <span data-ttu-id="1633b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1633b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1633b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1633b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1633b-128">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1633b-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1633b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1633b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1633b-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1633b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1633b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1633b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1633b-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1633b-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1633b-133">IDL</span><span class="sxs-lookup"><span data-stu-id="1633b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1633b-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1633b-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1633b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1633b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1633b-136"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1633b-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
