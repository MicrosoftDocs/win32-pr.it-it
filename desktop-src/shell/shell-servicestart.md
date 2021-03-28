---
description: Avvia un servizio denominato.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Metodo Shell. ServiceStart (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881905"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="20252-103">Shell. ServiceStart (metodo)</span><span class="sxs-lookup"><span data-stu-id="20252-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="20252-104">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="20252-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="20252-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20252-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="20252-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20252-107">*sServiceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20252-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20252-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="20252-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="20252-109">**Stringa** che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="20252-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="20252-110">*vPersistent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20252-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20252-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="20252-111">Type: **Variant**</span></span>

<span data-ttu-id="20252-112">Impostare su **true** per fare in modo che il servizio venga avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="20252-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="20252-113">Impostare su **false** per lasciare invariata la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="20252-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20252-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20252-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="20252-115">JScript</span><span class="sxs-lookup"><span data-stu-id="20252-115">JScript</span></span>

<span data-ttu-id="20252-116">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="20252-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="20252-117">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="20252-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="20252-118">VB</span><span class="sxs-lookup"><span data-stu-id="20252-118">VB</span></span>

<span data-ttu-id="20252-119">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="20252-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="20252-120">Restituisce _ *true*\* se ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="20252-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20252-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="20252-121">Remarks</span></span>

<span data-ttu-id="20252-122">Il metodo restituisce **false** se il servizio è già stato avviato.</span><span class="sxs-lookup"><span data-stu-id="20252-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="20252-123">Prima di chiamare questo metodo, è possibile chiamare [**Shell. IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="20252-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="20252-124">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="20252-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="20252-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="20252-125">Examples</span></span>

<span data-ttu-id="20252-126">Gli esempi seguenti illustrano l'uso di **ServiceStart** per avviare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="20252-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="20252-127">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="20252-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="20252-128">JScript</span><span class="sxs-lookup"><span data-stu-id="20252-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="20252-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="20252-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="20252-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20252-130">Requirements</span></span>



| <span data-ttu-id="20252-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="20252-131">Requirement</span></span> | <span data-ttu-id="20252-132">Valore</span><span class="sxs-lookup"><span data-stu-id="20252-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20252-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20252-133">Minimum supported client</span></span><br/> | <span data-ttu-id="20252-134">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="20252-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20252-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20252-135">Minimum supported server</span></span><br/> | <span data-ttu-id="20252-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20252-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="20252-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20252-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="20252-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="20252-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="20252-139">IDL</span><span class="sxs-lookup"><span data-stu-id="20252-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20252-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20252-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="20252-141">DLL</span><span class="sxs-lookup"><span data-stu-id="20252-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20252-142"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="20252-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
