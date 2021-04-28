---
description: 'Metodo IShellDispatch2.ServiceStart: avvia un servizio denominato.'
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Metodo IShellDispatch2.ServiceStart (Shldisp.h)
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
ms.openlocfilehash: c0f4fa218c4def993025ff18bffd0cc54def9818
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117049"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="180f0-103">Metodo IShellDispatch2.ServiceStart</span><span class="sxs-lookup"><span data-stu-id="180f0-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="180f0-104">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="180f0-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="180f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="180f0-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="180f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="180f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180f0-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="180f0-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="180f0-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="180f0-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="180f0-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="180f0-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="180f0-110">*vPersistent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="180f0-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="180f0-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="180f0-111">Type: **Variant**</span></span>

<span data-ttu-id="180f0-112">Impostare su **true per** fare in modo che il servizio sia avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="180f0-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="180f0-113">Impostare su **false per** lasciare invariata la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="180f0-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="180f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="180f0-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="180f0-115">JScript</span><span class="sxs-lookup"><span data-stu-id="180f0-115">JScript</span></span>

<span data-ttu-id="180f0-116">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="180f0-116">Type: **Variant\***</span></span>

<span data-ttu-id="180f0-117">Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="180f0-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="180f0-118">VB</span><span class="sxs-lookup"><span data-stu-id="180f0-118">VB</span></span>

<span data-ttu-id="180f0-119">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="180f0-119">Type: **Variant\***</span></span>

<span data-ttu-id="180f0-120">Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="180f0-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="180f0-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="180f0-121">Remarks</span></span>

<span data-ttu-id="180f0-122">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ServiceStart.**](./shell-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="180f0-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="180f0-123">Il metodo restituisce **false** se il servizio è già stato avviato.</span><span class="sxs-lookup"><span data-stu-id="180f0-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="180f0-124">Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="180f0-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="180f0-125">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="180f0-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="180f0-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="180f0-126">Examples</span></span>

<span data-ttu-id="180f0-127">Gli esempi seguenti illustrano l'uso **di ServiceStart** per avviare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="180f0-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="180f0-128">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="180f0-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="180f0-129">Jscript:</span><span class="sxs-lookup"><span data-stu-id="180f0-129">JScript:</span></span>


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



<span data-ttu-id="180f0-130">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="180f0-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="180f0-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="180f0-131">Requirements</span></span>



| <span data-ttu-id="180f0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="180f0-132">Requirement</span></span> | <span data-ttu-id="180f0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="180f0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180f0-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="180f0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="180f0-135">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="180f0-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="180f0-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="180f0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="180f0-137">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="180f0-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="180f0-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="180f0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="180f0-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="180f0-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="180f0-140">Idl</span><span class="sxs-lookup"><span data-stu-id="180f0-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="180f0-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="180f0-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="180f0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="180f0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="180f0-143"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="180f0-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
