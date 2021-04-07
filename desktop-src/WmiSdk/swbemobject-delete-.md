---
description: Il \_ metodo Delete dell'oggetto SWbemObject Elimina la classe corrente o l'istanza corrente.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Metodo SWbemObject.Delete_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057857"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="34f88-103">Metodo SWbemObject. Delete \_</span><span class="sxs-lookup"><span data-stu-id="34f88-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="34f88-104">Il **metodo \_ Delete** dell'oggetto [**SWbemObject**](swbemobject.md) Elimina la classe corrente o l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="34f88-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="34f88-105">Se un provider dinamico fornisce la classe o l'istanza, a volte non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.</span><span class="sxs-lookup"><span data-stu-id="34f88-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="34f88-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="34f88-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34f88-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34f88-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="34f88-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="34f88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f88-109">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="34f88-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34f88-110">Riservato e deve essere 0 (zero) se specificato.</span><span class="sxs-lookup"><span data-stu-id="34f88-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-111">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="34f88-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34f88-112">Questo parametro non è in genere definito.</span><span class="sxs-lookup"><span data-stu-id="34f88-112">This parameter is typically undefined.</span></span> <span data-ttu-id="34f88-113">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="34f88-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="34f88-114">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="34f88-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f88-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34f88-115">Return value</span></span>

<span data-ttu-id="34f88-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="34f88-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34f88-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="34f88-117">Error codes</span></span>

<span data-ttu-id="34f88-118">Dopo il completamento del **metodo \_ Delete** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="34f88-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="34f88-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="34f88-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-120">Il contesto corrente non dispone dei privilegi di protezione appropriati per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="34f88-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-121">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="34f88-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="34f88-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-123">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="34f88-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-124">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="34f88-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-125">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="34f88-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-126">Impossibile eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="34f88-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-127">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="34f88-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-128">Oggetto inesistente.</span><span class="sxs-lookup"><span data-stu-id="34f88-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="34f88-129">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="34f88-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="34f88-130">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="34f88-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34f88-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="34f88-131">Remarks</span></span>

<span data-ttu-id="34f88-132">Il **metodo \_ Delete** ha esito negativo se viene creata una nuova istanza di [**SWbemObject**](swbemobject.md) , ma non viene fornito alcun valore per la proprietà Key.</span><span class="sxs-lookup"><span data-stu-id="34f88-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="34f88-133">Strumentazione gestione Windows (WMI) genera automaticamente un valore di identificatore univoco globale (GUID), ma un valore GUID non viene accettato da **SWbemObject. Delete \_**.</span><span class="sxs-lookup"><span data-stu-id="34f88-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="34f88-134">In questo caso, [**SWbemServices. Delete**](swbemservices-delete.md), che usa il percorso dell'oggetto funziona.</span><span class="sxs-lookup"><span data-stu-id="34f88-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="34f88-135">Si noti che un oggetto [**SWbemObjectPath**](swbemobjectpath.md) viene restituito dal metodo [**SWbemObject. \_ put**](swbemobject-put-.md) dopo che è stato eseguito il commit di un oggetto in WMI.</span><span class="sxs-lookup"><span data-stu-id="34f88-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="34f88-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="34f88-136">Examples</span></span>

<span data-ttu-id="34f88-137">Nell'esempio seguente viene creata una nuova classe; aggiunge una proprietà chiave. scrive la nuova classe nel repository; e visualizza il percorso del nuovo oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="34f88-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="34f88-138">Lo script genera quindi un'istanza della nuova classe; scrive; e visualizza il percorso.</span><span class="sxs-lookup"><span data-stu-id="34f88-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="34f88-139">Si noti che lo script Elimina la classe e le relative istanze dal repository semplicemente eliminando la classe.</span><span class="sxs-lookup"><span data-stu-id="34f88-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="34f88-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34f88-140">Requirements</span></span>



| <span data-ttu-id="34f88-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="34f88-141">Requirement</span></span> | <span data-ttu-id="34f88-142">Valore</span><span class="sxs-lookup"><span data-stu-id="34f88-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34f88-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34f88-143">Minimum supported client</span></span><br/> | <span data-ttu-id="34f88-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34f88-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34f88-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34f88-145">Minimum supported server</span></span><br/> | <span data-ttu-id="34f88-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34f88-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34f88-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34f88-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="34f88-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34f88-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="34f88-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="34f88-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="34f88-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34f88-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34f88-151">DLL</span><span class="sxs-lookup"><span data-stu-id="34f88-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34f88-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34f88-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34f88-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="34f88-153">CLSID</span></span><br/>                    | <span data-ttu-id="34f88-154">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="34f88-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="34f88-155">IID</span><span class="sxs-lookup"><span data-stu-id="34f88-155">IID</span></span><br/>                      | <span data-ttu-id="34f88-156">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="34f88-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




