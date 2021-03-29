---
description: Arresta un servizio denominato.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Metodo IShellDispatch2. ServiceStop (shldisp. h)
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978018"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="cce15-103">IShellDispatch2. ServiceStop, metodo</span><span class="sxs-lookup"><span data-stu-id="cce15-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="cce15-104">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="cce15-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cce15-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="cce15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cce15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce15-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cce15-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce15-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cce15-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cce15-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="cce15-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="cce15-110">*vPersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cce15-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce15-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cce15-111">Type: **Variant**</span></span>

<span data-ttu-id="cce15-112">Impostare su **true** per fare in modo che il servizio venga avviato da Gestione controllo servizi quando viene chiamato il metodo [**ServiceStart**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="cce15-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="cce15-113">Per lasciare invariata la configurazione del servizio, impostare *vPersistent* su **false**.</span><span class="sxs-lookup"><span data-stu-id="cce15-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce15-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cce15-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cce15-115">JScript</span><span class="sxs-lookup"><span data-stu-id="cce15-115">JScript</span></span>

<span data-ttu-id="cce15-116">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="cce15-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="cce15-117">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cce15-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="cce15-118">VB</span><span class="sxs-lookup"><span data-stu-id="cce15-118">VB</span></span>

<span data-ttu-id="cce15-119">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="cce15-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="cce15-120">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cce15-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce15-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cce15-121">Remarks</span></span>

<span data-ttu-id="cce15-122">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ServiceStop**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="cce15-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="cce15-123">Il metodo restituisce **false** se il servizio è già stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="cce15-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="cce15-124">Prima di chiamare questo metodo, è possibile chiamare [**Shell. IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="cce15-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="cce15-125">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cce15-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cce15-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="cce15-126">Examples</span></span>

<span data-ttu-id="cce15-127">Gli esempi seguenti illustrano l'uso di **ServiceStop** per arrestare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="cce15-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="cce15-128">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="cce15-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="cce15-129">JScript</span><span class="sxs-lookup"><span data-stu-id="cce15-129">JScript:</span></span>


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



<span data-ttu-id="cce15-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="cce15-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cce15-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cce15-131">Requirements</span></span>



| <span data-ttu-id="cce15-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce15-132">Requirement</span></span> | <span data-ttu-id="cce15-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cce15-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce15-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce15-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cce15-135">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cce15-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cce15-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cce15-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cce15-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cce15-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cce15-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cce15-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce15-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce15-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cce15-140">IDL</span><span class="sxs-lookup"><span data-stu-id="cce15-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cce15-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cce15-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cce15-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cce15-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cce15-143"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="cce15-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
