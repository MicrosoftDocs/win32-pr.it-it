---
description: L'evento OnCompleted di un oggetto SWbemSink viene attivato al completamento di una chiamata asincrona. Questo evento indica all'applicazione client, il risultato di un'operazione asincrona e fornisce informazioni sull'errore quando la chiamata asincrona ha esito negativo.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnCompleted (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130966"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="9f108-104">Evento ISWbemSinkEvents:: OnCompleted</span><span class="sxs-lookup"><span data-stu-id="9f108-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="9f108-105">L'evento **OnCompleted** di un oggetto [**SWbemSink**](swbemsink.md) viene attivato al completamento di una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="9f108-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="9f108-106">Questo evento indica all'applicazione client, il risultato di un'operazione asincrona e fornisce informazioni sull'errore quando la chiamata asincrona ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9f108-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="9f108-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9f108-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f108-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f108-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="9f108-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f108-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f108-110">*iHResult*</span><span class="sxs-lookup"><span data-stu-id="9f108-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="9f108-111">HRESULT del metodo asincrono completato.</span><span class="sxs-lookup"><span data-stu-id="9f108-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="9f108-112">HRESULT corrisponde al valore restituito da un' [API com equivalente per](com-api-for-wmi.md) la chiamata al metodo WMI.</span><span class="sxs-lookup"><span data-stu-id="9f108-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="9f108-113">Controllare questo valore per determinare se la chiamata asincrona ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="9f108-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="9f108-114">Se la chiamata asincrona ha esito positivo, questo parametro contiene WBEM \_ S \_ senza \_ errori (0).</span><span class="sxs-lookup"><span data-stu-id="9f108-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="9f108-115">Se la chiamata asincrona ha esito negativo, questo parametro contiene un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="9f108-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="9f108-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="9f108-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="9f108-117">Contiene un oggetto [**SWbemLastError**](swbemlasterror.md) quando il metodo asincrono ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9f108-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="9f108-118">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="9f108-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9f108-119">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="9f108-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="9f108-120">Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f108-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f108-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f108-121">Return value</span></span>

<span data-ttu-id="9f108-122">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9f108-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9f108-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="9f108-123">Error codes</span></span>

<span data-ttu-id="9f108-124">Al termine dell'evento **OnCompleted** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="9f108-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="9f108-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9f108-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9f108-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9f108-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9f108-127">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9f108-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9f108-128">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9f108-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9f108-129">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="9f108-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="9f108-130">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="9f108-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f108-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f108-131">Remarks</span></span>

<span data-ttu-id="9f108-132">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="9f108-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="9f108-133">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9f108-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="9f108-134">Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="9f108-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="9f108-135">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9f108-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f108-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f108-136">Requirements</span></span>



| <span data-ttu-id="9f108-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f108-137">Requirement</span></span> | <span data-ttu-id="9f108-138">Valore</span><span class="sxs-lookup"><span data-stu-id="9f108-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f108-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f108-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9f108-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f108-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f108-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f108-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9f108-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f108-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f108-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f108-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f108-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f108-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f108-145">IDL</span><span class="sxs-lookup"><span data-stu-id="9f108-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f108-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f108-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f108-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9f108-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f108-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f108-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f108-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="9f108-149">CLSID</span></span><br/>                    | <span data-ttu-id="9f108-150">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="9f108-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="9f108-151">IID</span><span class="sxs-lookup"><span data-stu-id="9f108-151">IID</span></span><br/>                      | <span data-ttu-id="9f108-152">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="9f108-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

