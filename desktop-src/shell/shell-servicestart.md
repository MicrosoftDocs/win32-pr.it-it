---
description: 'Metodo Shell.ServiceStart: avvia un servizio denominato.'
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Metodo Shell.ServiceStart (Shldisp.h)
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
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083749"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="f5b69-103">Metodo Shell.ServiceStart</span><span class="sxs-lookup"><span data-stu-id="f5b69-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="f5b69-104">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="f5b69-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5b69-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="f5b69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5b69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b69-107">*sServiceName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5b69-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b69-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f5b69-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f5b69-109">Valore **String** contenente il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="f5b69-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="f5b69-110">*vPersistent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5b69-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b69-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="f5b69-111">Type: **Variant**</span></span>

<span data-ttu-id="f5b69-112">Impostare su **true per** fare in modo che il servizio sia avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5b69-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="f5b69-113">Impostare su **false per** lasciare invariata la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="f5b69-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b69-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5b69-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f5b69-115">JScript</span><span class="sxs-lookup"><span data-stu-id="f5b69-115">JScript</span></span>

<span data-ttu-id="f5b69-116">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="f5b69-116">Type: **Variant\***</span></span>

<span data-ttu-id="f5b69-117">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="f5b69-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="f5b69-118">VB</span><span class="sxs-lookup"><span data-stu-id="f5b69-118">VB</span></span>

<span data-ttu-id="f5b69-119">Tipo: **\* Variante**</span><span class="sxs-lookup"><span data-stu-id="f5b69-119">Type: **Variant\***</span></span>

<span data-ttu-id="f5b69-120">Restituisce **true se** ha esito positivo; in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="f5b69-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b69-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5b69-121">Remarks</span></span>

<span data-ttu-id="f5b69-122">Il metodo restituisce **false** se il servizio è già stato avviato.</span><span class="sxs-lookup"><span data-stu-id="f5b69-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="f5b69-123">Prima di chiamare questo metodo, è possibile chiamare [**Shell.IsServiceRunning**](./shell-isservicerunning.md) per verificare lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f5b69-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="f5b69-124">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f5b69-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f5b69-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5b69-125">Examples</span></span>

<span data-ttu-id="f5b69-126">Gli esempi seguenti illustrano l'uso **di ServiceStart** per avviare il servizio Messenger.</span><span class="sxs-lookup"><span data-stu-id="f5b69-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="f5b69-127">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="f5b69-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="f5b69-128">Jscript:</span><span class="sxs-lookup"><span data-stu-id="f5b69-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="f5b69-129">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="f5b69-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f5b69-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5b69-130">Requirements</span></span>



| <span data-ttu-id="f5b69-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b69-131">Requirement</span></span> | <span data-ttu-id="f5b69-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f5b69-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b69-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b69-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b69-134">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b69-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5b69-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5b69-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b69-136">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b69-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f5b69-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5b69-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5b69-138"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b69-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f5b69-139">Idl</span><span class="sxs-lookup"><span data-stu-id="f5b69-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5b69-140"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5b69-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f5b69-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b69-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b69-142"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f5b69-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
