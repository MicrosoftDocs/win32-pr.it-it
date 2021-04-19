---
description: Elimina la classe o l'istanza specificata nel percorso dell'oggetto. È possibile eliminare solo gli oggetti nello spazio dei nomi corrente.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Metodo SWbemServices. Delete (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485444"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="b4c96-104">Metodo SWbemServices. Delete</span><span class="sxs-lookup"><span data-stu-id="b4c96-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="b4c96-105">Il metodo **Delete** dell'oggetto [**SWbemServices**](swbemservices.md) Elimina la classe o l'istanza specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4c96-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="b4c96-106">È possibile eliminare solo gli oggetti nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="b4c96-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="b4c96-107">Se un provider dinamico fornisce la classe o l'istanza, non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.</span><span class="sxs-lookup"><span data-stu-id="b4c96-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="b4c96-108">Questo metodo viene chiamato in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="b4c96-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="b4c96-109">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b4c96-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b4c96-110">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b4c96-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c96-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4c96-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b4c96-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4c96-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c96-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="b4c96-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="b4c96-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4c96-114">Required.</span></span> <span data-ttu-id="b4c96-115">Stringa che contiene il percorso dell'oggetto che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="b4c96-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="b4c96-116">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="b4c96-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-117">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b4c96-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b4c96-118">Reserved.</span></span> <span data-ttu-id="b4c96-119">Il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b4c96-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-120">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="b4c96-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-121">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="b4c96-121">Typically, this is undefined.</span></span> <span data-ttu-id="b4c96-122">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b4c96-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="b4c96-123">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="b4c96-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c96-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4c96-124">Return value</span></span>

<span data-ttu-id="b4c96-125">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b4c96-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4c96-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b4c96-126">Error codes</span></span>

<span data-ttu-id="b4c96-127">Dopo il completamento del metodo **Delete** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="b4c96-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b4c96-128">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b4c96-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-129">Il contesto corrente non dispone dei privilegi di protezione appropriati per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4c96-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-130">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b4c96-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-131">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b4c96-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-132">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="b4c96-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-133">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="b4c96-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-134">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="b4c96-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-135">Impossibile eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4c96-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-136">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b4c96-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-137">Oggetto inesistente.</span><span class="sxs-lookup"><span data-stu-id="b4c96-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b4c96-138">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b4c96-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b4c96-139">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b4c96-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4c96-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4c96-140">Remarks</span></span>

<span data-ttu-id="b4c96-141">Il metodo **SWbemServices. Delete** può essere utilizzato quando alla proprietà della chiave per l'oggetto non viene assegnato un valore, perché questo metodo richiede solo un percorso di oggetto come input.</span><span class="sxs-lookup"><span data-stu-id="b4c96-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="b4c96-142">Questo metodo può essere utilizzato in situazioni in cui [**SWbemObject. \_ Delete**](swbemobject-delete-.md) non riesce per mancanza di un valore di chiave.</span><span class="sxs-lookup"><span data-stu-id="b4c96-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="b4c96-143">Se viene eseguito il commit dell'oggetto in WMI tramite [**SWbemObject \_ . Put**](swbemobject-put-.md), un oggetto [**SWbemObjectPath**](swbemobjectpath.md) è stato ottenuto tramite la chiamata.</span><span class="sxs-lookup"><span data-stu-id="b4c96-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="b4c96-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="b4c96-144">Examples</span></span>

<span data-ttu-id="b4c96-145">Nell'esempio seguente viene creata una nuova classe, viene aggiunta una proprietà che non è una chiave, viene scritta la nuova classe nel repository e viene visualizzato il percorso del nuovo oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="b4c96-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="b4c96-146">Lo script genera quindi un'istanza della nuova classe, scrive l'istanza e visualizza il percorso.</span><span class="sxs-lookup"><span data-stu-id="b4c96-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="b4c96-147">Si noti che lo script Elimina la classe e le relative istanze dal repository eliminando la classe.</span><span class="sxs-lookup"><span data-stu-id="b4c96-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="b4c96-148">Per ulteriori informazioni sulle classi e le istanze WMI, vedere la pagina relativa alla [modifica delle informazioni relative](manipulating-class-and-instance-information.md) a classi e istanze e [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="b4c96-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b4c96-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4c96-149">Requirements</span></span>



| <span data-ttu-id="b4c96-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c96-150">Requirement</span></span> | <span data-ttu-id="b4c96-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b4c96-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c96-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c96-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c96-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4c96-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4c96-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c96-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c96-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4c96-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4c96-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4c96-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c96-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c96-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4c96-158">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b4c96-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4c96-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4c96-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4c96-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b4c96-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4c96-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4c96-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4c96-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="b4c96-162">CLSID</span></span><br/>                    | <span data-ttu-id="b4c96-163">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="b4c96-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b4c96-164">IID</span><span class="sxs-lookup"><span data-stu-id="b4c96-164">IID</span></span><br/>                      | <span data-ttu-id="b4c96-165">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="b4c96-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b4c96-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4c96-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c96-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="b4c96-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b4c96-168">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="b4c96-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




