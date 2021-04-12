---
description: Il metodo Cancel dell'oggetto SWbemSink Annulla tutte le operazioni asincrone in attesa associate a questo sink di oggetto.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Metodo ISWbemSink:: Cancel (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233985"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="ba217-103">Metodo ISWbemSink:: Cancel</span><span class="sxs-lookup"><span data-stu-id="ba217-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="ba217-104">Il metodo **Cancel** dell'oggetto [**SWbemSink**](swbemsink.md) Annulla tutte le operazioni asincrone in attesa associate a questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba217-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="ba217-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ba217-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba217-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba217-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="ba217-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba217-107">Parameters</span></span>

<span data-ttu-id="ba217-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ba217-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba217-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba217-109">Return value</span></span>

<span data-ttu-id="ba217-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ba217-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba217-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba217-111">Error codes</span></span>

<span data-ttu-id="ba217-112">Dopo il completamento del metodo **Cancel** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ba217-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="ba217-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ba217-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ba217-114">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ba217-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ba217-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ba217-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ba217-116">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ba217-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba217-117">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="ba217-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="ba217-118">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="ba217-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba217-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ba217-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ba217-120">Il nome utente o la password corrente o specificata non sono validi o sono autorizzati a eseguire la connessione.</span><span class="sxs-lookup"><span data-stu-id="ba217-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba217-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba217-121">Remarks</span></span>

<span data-ttu-id="ba217-122">Non è possibile annullare una sola chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ba217-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="ba217-123">Se sono in sospeso più chiamate asincrone che usano questo sink di oggetto, questo metodo annulla tutte le chiamate asincrone che usano questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba217-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="ba217-124">Le chiamate asincrone associate ad altri sink di oggetto continuano a non essere interessate.</span><span class="sxs-lookup"><span data-stu-id="ba217-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="ba217-125">Non è possibile assegnare questo sink a **Nessun** elemento per annullare un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ba217-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="ba217-126">È necessario chiamare il metodo **Cancel** per fare in modo che WMI interrompa l'operazione e liberare le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="ba217-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="ba217-127">Questo è molto importante con operazioni asincrone lunghe, ad esempio query, o operazioni che non vengono mai completate, ad esempio [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="ba217-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba217-128">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="ba217-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="ba217-129">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ba217-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ba217-130">Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="ba217-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="ba217-131">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ba217-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="ba217-132">Nell'esempio seguente viene illustrato come annullare una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="ba217-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="ba217-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba217-133">Requirements</span></span>



| <span data-ttu-id="ba217-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba217-134">Requirement</span></span> | <span data-ttu-id="ba217-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ba217-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba217-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba217-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ba217-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba217-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba217-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba217-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ba217-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba217-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba217-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba217-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba217-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba217-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba217-142">IDL</span><span class="sxs-lookup"><span data-stu-id="ba217-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba217-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba217-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ba217-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ba217-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba217-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba217-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ba217-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="ba217-146">CLSID</span></span><br/>                    | <span data-ttu-id="ba217-147">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="ba217-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="ba217-148">IID</span><span class="sxs-lookup"><span data-stu-id="ba217-148">IID</span></span><br/>                      | <span data-ttu-id="ba217-149">\_ISWBEMSINK IID</span><span class="sxs-lookup"><span data-stu-id="ba217-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="ba217-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba217-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba217-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="ba217-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

