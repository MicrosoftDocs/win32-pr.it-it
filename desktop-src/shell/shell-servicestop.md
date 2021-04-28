---
description: 'Metodo Shell.ServiceStop: arresta un servizio denominato.'
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Metodo Shell.ServiceStop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104159"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="1acb7-103">Metodo Shell.ServiceStop</span><span class="sxs-lookup"><span data-stu-id="1acb7-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="1acb7-104">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="1acb7-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acb7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1acb7-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="1acb7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1acb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1acb7-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1acb7-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1acb7-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1acb7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1acb7-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="1acb7-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="1acb7-110">*vPersistent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1acb7-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1acb7-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="1acb7-111">Type: **Variant**</span></span>

<span data-ttu-id="1acb7-112">Impostare su **true per** fare in modo che il servizio sia avviato da Gestione controllo servizi quando viene [**chiamato ServiceStart.**](./shell-servicestart.md)</span><span class="sxs-lookup"><span data-stu-id="1acb7-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="1acb7-113">Per lasciare invariata la configurazione del servizio, *impostare vPersistent* su **false.**</span><span class="sxs-lookup"><span data-stu-id="1acb7-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1acb7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1acb7-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1acb7-115">JScript</span><span class="sxs-lookup"><span data-stu-id="1acb7-115">JScript</span></span>

<span data-ttu-id="1acb7-116">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="1acb7-116">Type: **Variant\***</span></span>

<span data-ttu-id="1acb7-117">Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1acb7-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="1acb7-118">VB</span><span class="sxs-lookup"><span data-stu-id="1acb7-118">VB</span></span>

<span data-ttu-id="1acb7-119">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="1acb7-119">Type: **Variant\***</span></span>

<span data-ttu-id="1acb7-120">Restituisce **true se** l'operazione ha esito positivo. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1acb7-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1acb7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1acb7-121">Remarks</span></span>

<span data-ttu-id="1acb7-122">Il metodo restituisce **false** se il servizio è già stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="1acb7-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="1acb7-123">Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="1acb7-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="1acb7-124">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1acb7-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1acb7-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="1acb7-125">Examples</span></span>

<span data-ttu-id="1acb7-126">Gli esempi seguenti illustrano l'uso **di ServiceStop** per arrestare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="1acb7-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="1acb7-127">L'utilizzo è illustrato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="1acb7-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="1acb7-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="1acb7-128">JScript:</span></span>


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



<span data-ttu-id="1acb7-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="1acb7-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1acb7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1acb7-130">Requirements</span></span>



| <span data-ttu-id="1acb7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acb7-131">Requirement</span></span> | <span data-ttu-id="1acb7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1acb7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acb7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1acb7-134">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1acb7-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1acb7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1acb7-136">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1acb7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1acb7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1acb7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1acb7-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1acb7-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1acb7-139">Idl</span><span class="sxs-lookup"><span data-stu-id="1acb7-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1acb7-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1acb7-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1acb7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1acb7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1acb7-142"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1acb7-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
