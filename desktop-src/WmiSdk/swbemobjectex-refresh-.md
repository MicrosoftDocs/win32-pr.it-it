---
description: Aggiorna i dati per gli oggetti che dispongono di dati forniti da un provider di prestazioni, ad esempio le classi del contatore delle prestazioni. È possibile ottenere i dati aggiornati più rapidamente e senza una chiamata a SWbemServices. Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Metodo SWbemObjectEx.Refresh_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309815"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="424aa-104">Metodo SWbemObjectEx. Refresh \_</span><span class="sxs-lookup"><span data-stu-id="424aa-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="424aa-105">Il **metodo \_ Refresh** di [**SWbemObjectEx**](swbemobjectex.md) aggiorna i dati per gli oggetti che dispongono di dati forniti da un provider di prestazioni, ad esempio le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="424aa-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="424aa-106">È possibile ottenere i dati aggiornati più rapidamente e senza una chiamata a [**SWbemServices. \_ Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="424aa-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="424aa-107">Per altre informazioni su questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="424aa-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="424aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="424aa-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="424aa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="424aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424aa-110">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="424aa-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="424aa-111">Flag di operazione riservati che, se specificati, devono essere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="424aa-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="424aa-112">*objWbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="424aa-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="424aa-113">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che imposta il contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="424aa-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424aa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="424aa-114">Return value</span></span>

<span data-ttu-id="424aa-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="424aa-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="424aa-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="424aa-116">Error codes</span></span>

<span data-ttu-id="424aa-117">Dopo il completamento del **metodo \_ Refresh** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="424aa-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="424aa-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="424aa-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="424aa-119">Il provider non è riuscito internamente, anche se l'operazione è valida.</span><span class="sxs-lookup"><span data-stu-id="424aa-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="424aa-120">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="424aa-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="424aa-121">Il formato richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="424aa-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="424aa-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="424aa-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="424aa-123">Uno dei parametri della chiamata non è corretto.</span><span class="sxs-lookup"><span data-stu-id="424aa-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="424aa-124">**wbemErrRefresherBusy** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="424aa-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="424aa-125">L'aggiornamento è impegnato in un'altra operazione.</span><span class="sxs-lookup"><span data-stu-id="424aa-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="424aa-126">**wbemPartialResults** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="424aa-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="424aa-127">Non tutti gli oggetti, gli enumeratori o gli aggiornamenti annidati sono stati aggiornati correttamente.</span><span class="sxs-lookup"><span data-stu-id="424aa-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="424aa-128">Questo valore restituito non è un errore, ma indica che l'operazione non è completa.</span><span class="sxs-lookup"><span data-stu-id="424aa-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="424aa-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="424aa-129">Examples</span></span>

<span data-ttu-id="424aa-130">Nell'esempio di codice di script seguente viene illustrato come ottenere i contatori delle prestazioni sia RAW che cotti per il processo di sistema.</span><span class="sxs-lookup"><span data-stu-id="424aa-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="424aa-131">Gli oggetti vengono aggiornati ogni due secondi e vengono visualizzate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="424aa-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="424aa-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="424aa-132">Requirements</span></span>



| <span data-ttu-id="424aa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="424aa-133">Requirement</span></span> | <span data-ttu-id="424aa-134">Valore</span><span class="sxs-lookup"><span data-stu-id="424aa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="424aa-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="424aa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="424aa-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="424aa-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="424aa-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="424aa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="424aa-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="424aa-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="424aa-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="424aa-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="424aa-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="424aa-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="424aa-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="424aa-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="424aa-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="424aa-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="424aa-143">DLL</span><span class="sxs-lookup"><span data-stu-id="424aa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="424aa-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424aa-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="424aa-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="424aa-145">CLSID</span></span><br/>                    | <span data-ttu-id="424aa-146">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="424aa-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="424aa-147">IID</span><span class="sxs-lookup"><span data-stu-id="424aa-147">IID</span></span><br/>                      | <span data-ttu-id="424aa-148">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="424aa-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="424aa-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="424aa-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="424aa-150">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="424aa-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="424aa-151">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="424aa-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

