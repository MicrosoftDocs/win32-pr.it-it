---
description: 'SWbemServices.Exemetodo cMethod : esegue un metodo esportato da un provider di metodi.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cMethod (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103639"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="822e9-103">SWbemServices.Exemetodo cMethod</span><span class="sxs-lookup"><span data-stu-id="822e9-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="822e9-104">Il **metodo ExecMethod** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="822e9-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="822e9-105">Questo metodo si blocca mentre viene eseguito il metodo inoltrato al provider appropriato.</span><span class="sxs-lookup"><span data-stu-id="822e9-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="822e9-106">Le informazioni e lo stato vengono quindi restituiti.</span><span class="sxs-lookup"><span data-stu-id="822e9-106">The information and status are then returned.</span></span> <span data-ttu-id="822e9-107">Il provider, anziché WMI, implementa il metodo .</span><span class="sxs-lookup"><span data-stu-id="822e9-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="822e9-108">Questo metodo viene chiamato in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="822e9-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="822e9-109">Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="822e9-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="822e9-110">Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="822e9-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="822e9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="822e9-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="822e9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="822e9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822e9-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="822e9-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="822e9-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="822e9-114">Required.</span></span> <span data-ttu-id="822e9-115">Stringa contenente il percorso dell'oggetto per il quale viene eseguito il metodo.</span><span class="sxs-lookup"><span data-stu-id="822e9-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="822e9-116">Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="822e9-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="822e9-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="822e9-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="822e9-118">Required.</span></span> <span data-ttu-id="822e9-119">Nome del metodo per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="822e9-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-120">*objWbemInParams* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="822e9-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="822e9-121">Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="822e9-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="822e9-122">Per impostazione predefinita, questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="822e9-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="822e9-123">Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="822e9-124">*iFlags* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="822e9-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="822e9-125">Riservato.</span><span class="sxs-lookup"><span data-stu-id="822e9-125">Reserved.</span></span> <span data-ttu-id="822e9-126">Il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="822e9-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-127">*objWbemNamedValueSet* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="822e9-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="822e9-128">In genere, questa operazione non è definita.</span><span class="sxs-lookup"><span data-stu-id="822e9-128">Typically, this is undefined.</span></span> <span data-ttu-id="822e9-129">In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="822e9-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="822e9-130">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="822e9-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822e9-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="822e9-131">Return value</span></span>

<span data-ttu-id="822e9-132">Se il metodo ha esito positivo, viene restituito un [**oggetto SWbemObject.**](swbemobject.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="822e9-133">L'oggetto restituito contiene i parametri out e il valore restituito per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="822e9-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="822e9-134">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="822e9-134">Error codes</span></span>

<span data-ttu-id="822e9-135">Dopo il completamento del **metodo ExecMethod,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="822e9-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="822e9-136">**wbemErrFailed** - 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="822e9-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-137">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="822e9-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="822e9-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-139">Classe specificata non valida.</span><span class="sxs-lookup"><span data-stu-id="822e9-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="822e9-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-141">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="822e9-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="822e9-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-143">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="822e9-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="822e9-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-145">Metodo richiesto non disponibile.</span><span class="sxs-lookup"><span data-stu-id="822e9-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="822e9-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="822e9-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="822e9-147">L'utente corrente non è stato autorizzato a eseguire il metodo .</span><span class="sxs-lookup"><span data-stu-id="822e9-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="822e9-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="822e9-148">Remarks</span></span>

<span data-ttu-id="822e9-149">Usare **SWbemServices.ExecMethod come** alternativa all'accesso diretto per l'esecuzione di un metodo [*provider*](gloss-p.md) nei casi in cui non è possibile eseguire direttamente un metodo.</span><span class="sxs-lookup"><span data-stu-id="822e9-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="822e9-150">Il **metodo ExecMethod** consente di ottenere i parametri di output, se forniti dal provider, con un linguaggio di scripting che non supporta i parametri di output.</span><span class="sxs-lookup"><span data-stu-id="822e9-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="822e9-151">In caso contrario, il metodo consigliato per richiamare un metodo è l'uso dell'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="822e9-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="822e9-152">Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze.](manipulating-class-and-instance-information.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="822e9-153">Ad esempio, l'esempio di codice seguente che chiama il metodo del provider [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) nel [**servizio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) usa l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="822e9-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="822e9-154">Questo esempio chiama **SWbemServices.ExecMethod per** eseguire il [**metodo StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="822e9-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="822e9-155">Si noti che è necessario un percorso di **oggetto perchéSWbemServices.ExecMethod** non funziona già sull'oggetto, aSWbemObject.Exe [**cMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="822e9-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="822e9-156">Il **SWbemServices.Exemetodo cMethod** richiede un percorso di oggetto.</span><span class="sxs-lookup"><span data-stu-id="822e9-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="822e9-157">Se lo script contiene già un [**oggetto SWbemObject,**](swbemobject.md) usare il [**SWbemObject.Exemetodo cMethod.**](swbemobject-execmethod-.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="822e9-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="822e9-158">Examples</span></span>

<span data-ttu-id="822e9-159">L'esempio seguente illustra **il metodo ExecMethod.**</span><span class="sxs-lookup"><span data-stu-id="822e9-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="822e9-160">Lo script crea un [**oggetto Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue il Blocco note.</span><span class="sxs-lookup"><span data-stu-id="822e9-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="822e9-161">Mostra la configurazione di un [**oggetto InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un [**oggetto OutParameters.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="822e9-162">Per uno script che mostra le stesse operazioni eseguite in modo asincrono, [**SWbemServices.ExecMethodAsync.**](swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="822e9-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="822e9-163">Per un esempio dell'uso dell'accesso diretto, vedere [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="822e9-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="822e9-164">Per un esempio della stessa operazione che usa [**un oggetto SWbemObject**](swbemobject.md), [**vedereSWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="822e9-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="822e9-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="822e9-165">Requirements</span></span>



| <span data-ttu-id="822e9-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="822e9-166">Requirement</span></span> | <span data-ttu-id="822e9-167">Valore</span><span class="sxs-lookup"><span data-stu-id="822e9-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="822e9-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="822e9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="822e9-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="822e9-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="822e9-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="822e9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="822e9-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="822e9-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="822e9-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="822e9-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="822e9-173"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="822e9-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="822e9-174">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="822e9-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="822e9-175"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="822e9-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="822e9-176">DLL</span><span class="sxs-lookup"><span data-stu-id="822e9-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="822e9-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822e9-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="822e9-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="822e9-178">CLSID</span></span><br/>                    | <span data-ttu-id="822e9-179">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="822e9-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="822e9-180">IID</span><span class="sxs-lookup"><span data-stu-id="822e9-180">IID</span></span><br/>                      | <span data-ttu-id="822e9-181">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="822e9-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="822e9-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="822e9-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822e9-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="822e9-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="822e9-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="822e9-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="822e9-185">Chiamata di un metodo provider</span><span class="sxs-lookup"><span data-stu-id="822e9-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="822e9-186">Modifica delle informazioni su classi e istanze</span><span class="sxs-lookup"><span data-stu-id="822e9-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

