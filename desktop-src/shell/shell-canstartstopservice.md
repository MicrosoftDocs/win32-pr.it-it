---
description: "Metodo Shell.CanStartStopService: determina se l'utente corrente può avviare e arrestare il servizio denominato."
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Metodo Shell.CanStartStopService (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083689"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="a32ae-103">Metodo Shell.CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="a32ae-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="a32ae-104">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="a32ae-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a32ae-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="a32ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a32ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32ae-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a32ae-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a32ae-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="a32ae-108">Type: **String**</span></span>

<span data-ttu-id="a32ae-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a32ae-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32ae-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a32ae-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a32ae-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a32ae-111">JScript</span></span>

<span data-ttu-id="a32ae-112">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="a32ae-112">Type: **Variant\***</span></span>

<span data-ttu-id="a32ae-113">Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="a32ae-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="a32ae-114">VB</span><span class="sxs-lookup"><span data-stu-id="a32ae-114">VB</span></span>

<span data-ttu-id="a32ae-115">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="a32ae-115">Type: **Variant\***</span></span>

<span data-ttu-id="a32ae-116">Restituisce **true se** l'utente può avviare e arrestare il servizio. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="a32ae-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32ae-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a32ae-117">Remarks</span></span>

<span data-ttu-id="a32ae-118">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a32ae-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a32ae-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="a32ae-119">Examples</span></span>

<span data-ttu-id="a32ae-120">Negli esempi seguenti viene illustrato l'utilizzo **di CanStartStopService** per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="a32ae-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="a32ae-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a32ae-121">JScript:</span></span>


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



<span data-ttu-id="a32ae-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a32ae-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a32ae-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a32ae-123">Requirements</span></span>



| <span data-ttu-id="a32ae-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32ae-124">Requirement</span></span> | <span data-ttu-id="a32ae-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a32ae-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32ae-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32ae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a32ae-127">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a32ae-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a32ae-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32ae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a32ae-129">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a32ae-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a32ae-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a32ae-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32ae-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a32ae-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a32ae-132">Idl</span><span class="sxs-lookup"><span data-stu-id="a32ae-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a32ae-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a32ae-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a32ae-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a32ae-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a32ae-135"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a32ae-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




