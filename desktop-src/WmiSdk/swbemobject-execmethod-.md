---
description: Il \_ Metodo ExecMethod dell'oggetto SWbemObject esegue un metodo esportato da un provider di metodi.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Metodo SWbemObject.ExecMethod_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130983"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="ee6ef-103">Metodo cMethod SWbemObject.Exe\_</span><span class="sxs-lookup"><span data-stu-id="ee6ef-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="ee6ef-104">Il **metodo \_ ExecMethod** dell'oggetto [**SWbemObject**](swbemobject.md) esegue un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="ee6ef-105">Questo metodo viene sospeso mentre viene eseguito il metodo che viene inviato al provider appropriato.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="ee6ef-106">Le informazioni e lo stato vengono quindi restituiti.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-106">The information and status are then returned.</span></span> <span data-ttu-id="ee6ef-107">Il provider anziché WMI implementa il metodo.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="ee6ef-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ee6ef-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee6ef-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ee6ef-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee6ef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6ef-111">*strMethodName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee6ef-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-112">Required.</span></span> <span data-ttu-id="ee6ef-113">Nome del metodo per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-114">*objwbemInParams* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ee6ef-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-115">Si tratta di un oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="ee6ef-116">Per impostazione predefinita, questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="ee6ef-117">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ee6ef-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-118">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ee6ef-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-119">Riservato e deve essere impostato su 0 (zero) se specificato.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-120">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ee6ef-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-121">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-121">Typically, it is undefined.</span></span> <span data-ttu-id="ee6ef-122">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ee6ef-123">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee6ef-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee6ef-124">Return value</span></span>

<span data-ttu-id="ee6ef-125">Se questo metodo ha esito positivo, viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ee6ef-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="ee6ef-126">L'oggetto restituito contiene i parametri out e il valore restituito per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee6ef-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ee6ef-127">Error codes</span></span>

<span data-ttu-id="ee6ef-128">Dopo il completamento del metodo **ExecMethod \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ee6ef-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-131">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-132">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-134">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-135">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-136">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-137">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-138">Il metodo richiesto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="ee6ef-139">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ee6ef-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ee6ef-140">L'utente corrente non è autorizzato a eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee6ef-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee6ef-141">Remarks</span></span>

<span data-ttu-id="ee6ef-142">Questo metodo è simile a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), ma opera direttamente sull'oggetto il cui metodo deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="ee6ef-143">Nell'esempio di codice seguente, ad esempio, viene chiamato il metodo del provider [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) nel [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) e viene utilizzato l' [accesso diretto](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="ee6ef-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="ee6ef-144">Questa versione chiama **SWbemObject.ExecMethod \_** per eseguire il metodo [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="ee6ef-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="ee6ef-145">Usare **SWbemObject.ExecMethod \_** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) nei casi in cui non è possibile eseguire direttamente un metodo.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="ee6ef-146">Ad esempio, è possibile usare **SWbemObject.ExecMethod \_** con un linguaggio di scripting che non supporta i parametri di output se il metodo ha parametri out.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="ee6ef-147">In caso contrario, la modalità consigliata per richiamare un metodo consiste nell'utilizzare l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="ee6ef-148">Il **SWbemObject.Exemetodo \_ cMethod** presuppone che l'oggetto rappresentato da [**SWbemObject**](swbemobject.md) contenga il metodo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="ee6ef-149">Al contrario, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) richiede un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="ee6ef-150">Usare **SWbemObject.ExecMethod \_** se è già stato ottenuto l'oggetto di cui si vuole eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="ee6ef-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee6ef-151">Examples</span></span>

<span data-ttu-id="ee6ef-152">Nell'esempio seguente viene illustrato il metodo [**ExecMethod**](swbemservices-execmethod.md) . Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="ee6ef-153">Per ulteriori informazioni su uno script che illustra le stesse operazioni eseguite in modo asincrono, vedere [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="ee6ef-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="ee6ef-154">Per un esempio di utilizzo dell'accesso diretto, vedere [**creare un metodo nella classe \_ processo Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="ee6ef-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="ee6ef-155">Per un esempio della stessa operazione usando un oggetto [**SWbemServices**](swbemservices.md) , vedere **SWbemServices.ExecMethod**.</span><span class="sxs-lookup"><span data-stu-id="ee6ef-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="ee6ef-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee6ef-156">Requirements</span></span>



| <span data-ttu-id="ee6ef-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee6ef-157">Requirement</span></span> | <span data-ttu-id="ee6ef-158">Valore</span><span class="sxs-lookup"><span data-stu-id="ee6ef-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6ef-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee6ef-159">Minimum supported client</span></span><br/> | <span data-ttu-id="ee6ef-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee6ef-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee6ef-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee6ef-161">Minimum supported server</span></span><br/> | <span data-ttu-id="ee6ef-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee6ef-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee6ef-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee6ef-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee6ef-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee6ef-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee6ef-165">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ee6ef-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee6ef-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee6ef-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee6ef-167">DLL</span><span class="sxs-lookup"><span data-stu-id="ee6ef-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee6ef-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee6ef-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee6ef-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="ee6ef-169">CLSID</span></span><br/>                    | <span data-ttu-id="ee6ef-170">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="ee6ef-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ee6ef-171">IID</span><span class="sxs-lookup"><span data-stu-id="ee6ef-171">IID</span></span><br/>                      | <span data-ttu-id="ee6ef-172">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="ee6ef-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ee6ef-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee6ef-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6ef-174">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ee6ef-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="ee6ef-175">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ee6ef-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="ee6ef-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="ee6ef-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

