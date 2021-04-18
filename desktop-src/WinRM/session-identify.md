---
title: Metodo Session. identifi (WSManDisp. h)
description: Esegue una query su un computer remoto per determinare se supporta il protocollo WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identifica Gestione remota Windows del metodo
- Identifica Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo di identificazione
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302401"
---
# <a name="sessionidentify-method"></a><span data-ttu-id="76ab3-106">Metodo Session. identifi</span><span class="sxs-lookup"><span data-stu-id="76ab3-106">Session.Identify method</span></span>

<span data-ttu-id="76ab3-107">Il metodo **Session. identifi** esegue una query su un computer remoto per determinare se supporta il protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="76ab3-107">The **Session.Identify** method queries a remote computer to determine if it supports the WS-Management protocol.</span></span> <span data-ttu-id="76ab3-108">Per ulteriori informazioni, vedere [rilevare se un computer remoto supporta il protocollo WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="76ab3-108">For more information, see [Detecting Whether a Remote Computer Supports WS-Management Protocol](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76ab3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76ab3-109">Syntax</span></span>


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="76ab3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="76ab3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ab3-111">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76ab3-111">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76ab3-112">Per inviare la richiesta in modalità autenticata, usare la costante di autenticazione dell'enumerazione **WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="76ab3-112">To send the request in authenticated mode use authentication constant from the **WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="76ab3-113">Per inviare in modalità non autenticata, usare **WSManFlagUseNoAuthentication**.</span><span class="sxs-lookup"><span data-stu-id="76ab3-113">To send in unauthenticated mode, use **WSManFlagUseNoAuthentication**.</span></span> <span data-ttu-id="76ab3-114">Per altre informazioni, vedere [**costanti di autenticazione**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="76ab3-114">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ab3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76ab3-115">Return value</span></span>

<span data-ttu-id="76ab3-116">Stringa XML che specifica la versione del protocollo WS-Management, il fornitore del sistema operativo e, se la richiesta è stata inviata autenticata, la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76ab3-116">An XML string that specifies the WS-Management protocol version, the operating system vendor and, if the request was sent authenticated, the operating system version.</span></span>

## <a name="remarks"></a><span data-ttu-id="76ab3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="76ab3-117">Remarks</span></span>

<span data-ttu-id="76ab3-118">**Session. identifit** si basa sull'operazione [protocollo WS-Management](ws-management-protocol.md) definita come wsmanIdentity.</span><span class="sxs-lookup"><span data-stu-id="76ab3-118">**Session.Identify** is based on the [WS-Management Protocol](ws-management-protocol.md) operation defined as wsmanIdentity.</span></span> <span data-ttu-id="76ab3-119">Questa operazione viene specificata nel pacchetto SOAP, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="76ab3-119">This is specified in the SOAP packet as follows:</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a><span data-ttu-id="76ab3-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="76ab3-120">Examples</span></span>

<span data-ttu-id="76ab3-121">Nell'esempio VBScript seguente viene inviata una richiesta di identificazione non autenticata al computer remoto denominato Remote nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="76ab3-121">The following VBScript example sends an unauthenticated Identify request to the remote computer named Remote in the same domain.</span></span>


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a><span data-ttu-id="76ab3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76ab3-122">Requirements</span></span>



| <span data-ttu-id="76ab3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ab3-123">Requirement</span></span> | <span data-ttu-id="76ab3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="76ab3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ab3-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ab3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76ab3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76ab3-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="76ab3-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ab3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76ab3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76ab3-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="76ab3-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76ab3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ab3-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ab3-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="76ab3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="76ab3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76ab3-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76ab3-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="76ab3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="76ab3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="76ab3-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76ab3-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76ab3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="76ab3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76ab3-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76ab3-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76ab3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76ab3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ab3-138">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="76ab3-138">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="76ab3-139">**IWSManSession:: identifica**</span><span class="sxs-lookup"><span data-stu-id="76ab3-139">**IWSManSession::Identify**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[<span data-ttu-id="76ab3-140">Protocollo WS-Management</span><span class="sxs-lookup"><span data-stu-id="76ab3-140">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

 





