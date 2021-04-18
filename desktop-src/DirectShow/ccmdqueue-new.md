---
description: Il nuovo metodo inizializza un comando da eseguire e restituisce un nuovo oggetto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Metodo CCmdQueue. New (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324474"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="72bdb-103">CCmdQueue. New, metodo</span><span class="sxs-lookup"><span data-stu-id="72bdb-103">CCmdQueue.New method</span></span>

<span data-ttu-id="72bdb-104">Il `New` Metodo Inizializza un comando da eseguire e restituisce un nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="72bdb-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="72bdb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72bdb-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="72bdb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72bdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72bdb-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="72bdb-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-108">Indirizzo di un puntatore a un oggetto [**CDeferredCommand**](cdeferredcommand.md) tramite il quale un'applicazione può annullare il comando, impostare una nuova ora di presentazione per esso oppure recuperare le informazioni relative alla stima.</span><span class="sxs-lookup"><span data-stu-id="72bdb-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="72bdb-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-110">Puntatore all'oggetto che eseguirà il comando.</span><span class="sxs-lookup"><span data-stu-id="72bdb-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-111">*time*</span><span class="sxs-lookup"><span data-stu-id="72bdb-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-112">Ora in cui eseguire il comando o i comandi in coda.</span><span class="sxs-lookup"><span data-stu-id="72bdb-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-113">*IID*</span><span class="sxs-lookup"><span data-stu-id="72bdb-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-114">Puntatore all'identificatore univoco globale (**GUID**) dell'interfaccia da chiamare.</span><span class="sxs-lookup"><span data-stu-id="72bdb-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-115">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="72bdb-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-116">Metodo sull'interfaccia da chiamare.</span><span class="sxs-lookup"><span data-stu-id="72bdb-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="72bdb-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-118">Flag che descrivono il contesto della chiamata.</span><span class="sxs-lookup"><span data-stu-id="72bdb-118">Flags describing the context of the call.</span></span> <span data-ttu-id="72bdb-119">Questo parametro supporta gli stessi flag del metodo **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="72bdb-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-120">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="72bdb-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-121">Numero di argomenti passati.</span><span class="sxs-lookup"><span data-stu-id="72bdb-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-122">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="72bdb-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-123">Puntatore all'elenco di tipi Variant associati ai parametri di invio.</span><span class="sxs-lookup"><span data-stu-id="72bdb-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-124">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="72bdb-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-125">Puntatore all'elenco in cui devono essere restituiti i risultati, se presenti.</span><span class="sxs-lookup"><span data-stu-id="72bdb-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-126">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="72bdb-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-127">Puntatore all'indice all'interno dell'elenco di parametri *pDispParams* in cui si è verificato l'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="72bdb-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="72bdb-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="72bdb-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="72bdb-129">Valore che indica se il parametro di *ora* è un valore in fase di flusso (**true**) o un valore della fase di presentazione (**false**).</span><span class="sxs-lookup"><span data-stu-id="72bdb-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72bdb-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72bdb-130">Return value</span></span>

<span data-ttu-id="72bdb-131">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="72bdb-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="72bdb-132">Restituisce E \_ OutOfMemory se *ppCmd* restituisce un valore **null** per la creazione del nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="72bdb-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="72bdb-133">In caso contrario, restituisce un valore **HRESULT** che indica un errore durante il tentativo di creazione di un nuovo oggetto **CDeferredCommand** .</span><span class="sxs-lookup"><span data-stu-id="72bdb-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="72bdb-134">Se si verifica un errore, nessun oggetto è stato accodato.</span><span class="sxs-lookup"><span data-stu-id="72bdb-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="72bdb-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="72bdb-135">Remarks</span></span>

<span data-ttu-id="72bdb-136">Il nuovo oggetto [**CDeferredCommand**](cdeferredcommand.md) verrà inizializzato con i parametri e verrà aggiunto alla coda durante la costruzione.</span><span class="sxs-lookup"><span data-stu-id="72bdb-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="72bdb-137">Questo metodo è simile al metodo **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="72bdb-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="72bdb-138">I valori per il parametro *wFlags* sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="72bdb-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="72bdb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="72bdb-139">Value</span></span>                    | <span data-ttu-id="72bdb-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72bdb-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bdb-141">\_metodo Dispatch</span><span class="sxs-lookup"><span data-stu-id="72bdb-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="72bdb-142">Il membro viene eseguito come metodo.</span><span class="sxs-lookup"><span data-stu-id="72bdb-142">The member is being run as a method.</span></span> <span data-ttu-id="72bdb-143">Se una proprietà ha lo stesso nome, è possibile impostare sia questo che il \_ flag PropertyGet (di invio.</span><span class="sxs-lookup"><span data-stu-id="72bdb-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="72bdb-144">\_PROPERTYGET (dispatch</span><span class="sxs-lookup"><span data-stu-id="72bdb-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="72bdb-145">Il membro viene recuperato come una proprietà o un membro dati.</span><span class="sxs-lookup"><span data-stu-id="72bdb-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="72bdb-146">\_PROPERTYPUT dispatch</span><span class="sxs-lookup"><span data-stu-id="72bdb-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="72bdb-147">Il membro viene modificato come una proprietà o un membro dati.</span><span class="sxs-lookup"><span data-stu-id="72bdb-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="72bdb-148">\_PROPERTYPUTREF dispatch</span><span class="sxs-lookup"><span data-stu-id="72bdb-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="72bdb-149">Il membro viene modificato tramite un'assegnazione di riferimento, anziché un'assegnazione di valore.</span><span class="sxs-lookup"><span data-stu-id="72bdb-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="72bdb-150">Questo valore è valido solo quando la proprietà accetta un riferimento a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="72bdb-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="72bdb-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72bdb-151">Requirements</span></span>



| <span data-ttu-id="72bdb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="72bdb-152">Requirement</span></span> | <span data-ttu-id="72bdb-153">Valore</span><span class="sxs-lookup"><span data-stu-id="72bdb-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bdb-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72bdb-154">Header</span></span><br/>  | <dl> <span data-ttu-id="72bdb-155"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72bdb-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72bdb-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="72bdb-156">Library</span></span><br/> | <dl> <span data-ttu-id="72bdb-157"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72bdb-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72bdb-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72bdb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bdb-159">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="72bdb-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




