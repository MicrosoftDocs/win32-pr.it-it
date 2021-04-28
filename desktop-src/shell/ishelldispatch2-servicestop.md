---
description: 'Metodo IShellDispatch2.ServiceStop: arresta un servizio denominato.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Metodo IShellDispatch2.ServiceStop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117029"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="64554-103">Metodo IShellDispatch2.ServiceStop</span><span class="sxs-lookup"><span data-stu-id="64554-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="64554-104">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="64554-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="64554-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64554-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="64554-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64554-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64554-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="64554-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64554-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="64554-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="64554-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="64554-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="64554-110">*vPersistent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="64554-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64554-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="64554-111">Type: **Variant**</span></span>

<span data-ttu-id="64554-112">Impostare su **true per** fare in modo che il servizio sia avviato da Gestione controllo servizi quando viene [**chiamato ServiceStart.**](ishelldispatch2-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="64554-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="64554-113">Per lasciare invariata la configurazione del servizio, *impostare vPersistent* su **false.**</span><span class="sxs-lookup"><span data-stu-id="64554-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64554-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64554-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="64554-115">JScript</span><span class="sxs-lookup"><span data-stu-id="64554-115">JScript</span></span>

<span data-ttu-id="64554-116">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="64554-116">Type: **Variant\***</span></span>

<span data-ttu-id="64554-117">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="64554-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="64554-118">VB</span><span class="sxs-lookup"><span data-stu-id="64554-118">VB</span></span>

<span data-ttu-id="64554-119">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="64554-119">Type: **Variant\***</span></span>

<span data-ttu-id="64554-120">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="64554-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="64554-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="64554-121">Remarks</span></span>

<span data-ttu-id="64554-122">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ServiceStop.**](./shell-servicestop.md)</span><span class="sxs-lookup"><span data-stu-id="64554-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="64554-123">Il metodo restituisce **false** se il servizio è già stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="64554-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="64554-124">Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="64554-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="64554-125">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64554-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="64554-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="64554-126">Examples</span></span>

<span data-ttu-id="64554-127">Gli esempi seguenti illustrano l'uso **di ServiceStop** per arrestare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="64554-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="64554-128">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="64554-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="64554-129">Jscript:</span><span class="sxs-lookup"><span data-stu-id="64554-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="64554-130">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="64554-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="64554-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64554-131">Requirements</span></span>



| <span data-ttu-id="64554-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="64554-132">Requirement</span></span> | <span data-ttu-id="64554-133">Valore</span><span class="sxs-lookup"><span data-stu-id="64554-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64554-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64554-134">Minimum supported client</span></span><br/> | <span data-ttu-id="64554-135">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="64554-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64554-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64554-136">Minimum supported server</span></span><br/> | <span data-ttu-id="64554-137">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="64554-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="64554-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64554-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="64554-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="64554-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="64554-140">Idl</span><span class="sxs-lookup"><span data-stu-id="64554-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64554-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="64554-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="64554-142">DLL</span><span class="sxs-lookup"><span data-stu-id="64554-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64554-143"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="64554-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
