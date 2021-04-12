---
description: L'evento OnObjectPut di un oggetto SWbemSink viene attivato al completamento di un'operazione di inserimento asincrona. Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectPut (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233984"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="87ebd-104">Evento ISWbemSinkEvents:: OnObjectPut</span><span class="sxs-lookup"><span data-stu-id="87ebd-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="87ebd-105">L'evento **OnObjectPut** di un oggetto [**SWbemSink**](swbemsink.md) viene attivato al completamento di un'operazione di inserimento asincrona.</span><span class="sxs-lookup"><span data-stu-id="87ebd-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="87ebd-106">Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata.</span><span class="sxs-lookup"><span data-stu-id="87ebd-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="87ebd-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="87ebd-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="87ebd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87ebd-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="87ebd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="87ebd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ebd-110">*objWbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="87ebd-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="87ebd-111">Oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto dell'istanza o della classe che l'operazione PUT scrive in WMI.</span><span class="sxs-lookup"><span data-stu-id="87ebd-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="87ebd-112">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="87ebd-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="87ebd-113">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="87ebd-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="87ebd-114">Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="87ebd-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ebd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87ebd-115">Return value</span></span>

<span data-ttu-id="87ebd-116">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="87ebd-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87ebd-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="87ebd-117">Error codes</span></span>

<span data-ttu-id="87ebd-118">Al termine dell'evento **OnObjectPut** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="87ebd-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="87ebd-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="87ebd-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="87ebd-120">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="87ebd-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="87ebd-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="87ebd-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="87ebd-122">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="87ebd-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87ebd-123">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="87ebd-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="87ebd-124">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="87ebd-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87ebd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="87ebd-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87ebd-126">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="87ebd-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="87ebd-127">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="87ebd-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="87ebd-128">Per eliminare i rischi, usare la comunicazione semi-sincrona o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="87ebd-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="87ebd-129">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="87ebd-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87ebd-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87ebd-130">Requirements</span></span>



| <span data-ttu-id="87ebd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ebd-131">Requirement</span></span> | <span data-ttu-id="87ebd-132">Valore</span><span class="sxs-lookup"><span data-stu-id="87ebd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ebd-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ebd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="87ebd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87ebd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87ebd-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ebd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="87ebd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87ebd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87ebd-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87ebd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ebd-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87ebd-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87ebd-139">IDL</span><span class="sxs-lookup"><span data-stu-id="87ebd-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87ebd-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87ebd-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="87ebd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="87ebd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87ebd-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ebd-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87ebd-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="87ebd-143">CLSID</span></span><br/>                    | <span data-ttu-id="87ebd-144">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="87ebd-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="87ebd-145">IID</span><span class="sxs-lookup"><span data-stu-id="87ebd-145">IID</span></span><br/>                      | <span data-ttu-id="87ebd-146">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="87ebd-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="87ebd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87ebd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ebd-148">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="87ebd-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

