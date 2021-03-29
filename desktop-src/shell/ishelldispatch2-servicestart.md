---
description: Avvia un servizio denominato.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Metodo IShellDispatch2. ServiceStart (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978026"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="9cc14-103">IShellDispatch2. ServiceStart, metodo</span><span class="sxs-lookup"><span data-stu-id="9cc14-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="9cc14-104">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="9cc14-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc14-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="9cc14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cc14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc14-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cc14-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc14-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9cc14-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9cc14-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="9cc14-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9cc14-110">*vPersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cc14-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc14-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9cc14-111">Type: **Variant**</span></span>

<span data-ttu-id="9cc14-112">Impostare su **true** per fare in modo che il servizio venga avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="9cc14-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="9cc14-113">Impostare su **false** per lasciare invariata la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="9cc14-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc14-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cc14-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9cc14-115">JScript</span><span class="sxs-lookup"><span data-stu-id="9cc14-115">JScript</span></span>

<span data-ttu-id="9cc14-116">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="9cc14-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="9cc14-117">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9cc14-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="9cc14-118">VB</span><span class="sxs-lookup"><span data-stu-id="9cc14-118">VB</span></span>

<span data-ttu-id="9cc14-119">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="9cc14-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="9cc14-120">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9cc14-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc14-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cc14-121">Remarks</span></span>

<span data-ttu-id="9cc14-122">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="9cc14-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="9cc14-123">Il metodo restituisce **false** se il servizio è già stato avviato.</span><span class="sxs-lookup"><span data-stu-id="9cc14-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="9cc14-124">Prima di chiamare questo metodo, è possibile chiamare [**Shell. IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="9cc14-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="9cc14-125">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9cc14-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="9cc14-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="9cc14-126">Examples</span></span>

<span data-ttu-id="9cc14-127">Gli esempi seguenti illustrano l'uso di **ServiceStart** per avviare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="9cc14-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="9cc14-128">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="9cc14-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="9cc14-129">JScript</span><span class="sxs-lookup"><span data-stu-id="9cc14-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="9cc14-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="9cc14-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="9cc14-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc14-131">Requirements</span></span>



| <span data-ttu-id="9cc14-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc14-132">Requirement</span></span> | <span data-ttu-id="9cc14-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc14-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc14-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc14-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc14-135">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9cc14-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cc14-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc14-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc14-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cc14-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9cc14-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cc14-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc14-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc14-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9cc14-140">IDL</span><span class="sxs-lookup"><span data-stu-id="9cc14-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9cc14-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9cc14-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9cc14-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc14-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc14-143"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc14-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
