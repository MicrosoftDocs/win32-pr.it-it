---
description: "Il metodo IWiaDevMgr2:: RegisterEventCallbackProgram registra un'applicazione per la ricezione di eventi del dispositivo. Viene fornita principalmente per garantire la compatibilità con le applicazioni che non sono state scritte per Windows Image Acquisition (WIA) 2,0."
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackProgram (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308235"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="80558-104">Metodo IWiaDevMgr2:: RegisterEventCallbackProgram</span><span class="sxs-lookup"><span data-stu-id="80558-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="80558-105">Il metodo **IWiaDevMgr2:: RegisterEventCallbackProgram** registra un'applicazione per la ricezione di eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80558-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="80558-106">Viene fornita principalmente per garantire la compatibilità con le applicazioni che non sono state scritte per Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="80558-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="80558-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80558-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="80558-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="80558-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80558-109">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-110">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="80558-110">Type: **LONG**</span></span>

<span data-ttu-id="80558-111">Flag di registrazione.</span><span class="sxs-lookup"><span data-stu-id="80558-111">The registration flags.</span></span> <span data-ttu-id="80558-112">Può essere impostato sui valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80558-112">Can be set to the following values.</span></span>



| <span data-ttu-id="80558-113">Valore</span><span class="sxs-lookup"><span data-stu-id="80558-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="80558-114">Significato</span><span class="sxs-lookup"><span data-stu-id="80558-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="80558-115"><dt>**\_callback di \_ evento di registro WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80558-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="80558-116">Eseguire la registrazione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="80558-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="80558-117"><dt>**\_callback di evento WIA Annulla registrazione \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80558-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="80558-118">Eliminare la registrazione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="80558-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="80558-119"><dt>**\_ \_ gestore predefinito set \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="80558-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="80558-120">Impostare l'applicazione come gestore eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="80558-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80558-121">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-122">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-122">Type: **BSTR**</span></span>

<span data-ttu-id="80558-123">Identificatore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80558-123">A device identifier.</span></span> <span data-ttu-id="80558-124">Passare **null** per eseguire la registrazione per l'evento in tutti i dispositivi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="80558-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="80558-125">*pEventGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-126">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="80558-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="80558-127">Evento per cui è registrata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-127">The event that the application is registering for.</span></span> <span data-ttu-id="80558-128">Per un elenco di GUID evento validi, vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="80558-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="80558-129">_bstrFullAppName \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-130">Type: **BSTR**</span></span>

<span data-ttu-id="80558-131">Nome completo del percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="80558-132">*bstrCommandlineArg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-133">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-133">Type: **BSTR**</span></span>

<span data-ttu-id="80558-134">Argomenti della riga di comando appropriati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="80558-135">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-136">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-136">Type: **BSTR**</span></span>

<span data-ttu-id="80558-137">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-137">The name of the application.</span></span> <span data-ttu-id="80558-138">Il nome viene visualizzato all'utente quando più applicazioni si registrano per lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="80558-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="80558-139">*bstrDescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-140">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-140">Type: **BSTR**</span></span>

<span data-ttu-id="80558-141">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-141">The description of the application.</span></span> <span data-ttu-id="80558-142">La descrizione viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="80558-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="80558-143">*bstrIcon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80558-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80558-144">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80558-144">Type: **BSTR**</span></span>

<span data-ttu-id="80558-145">Icona che rappresenta l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-145">The icon that represents the application.</span></span> <span data-ttu-id="80558-146">L'icona viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="80558-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="80558-147">La stringa contiene il nome dell'applicazione e l'indice in base zero dell'icona separata da una virgola, ad esempio "MyApp,0".</span><span class="sxs-lookup"><span data-stu-id="80558-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="80558-148">Potrebbe esserci più di un'icona che rappresenta un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80558-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80558-149">Return value</span></span>

<span data-ttu-id="80558-150">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80558-150">Type: **HRESULT**</span></span>

<span data-ttu-id="80558-151">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80558-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80558-152">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80558-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80558-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="80558-153">Remarks</span></span>

<span data-ttu-id="80558-154">Usare **IWiaDevMgr2:: RegisterEventCallbackProgram** per registrare gli eventi relativi ai dispositivi hardware.</span><span class="sxs-lookup"><span data-stu-id="80558-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="80558-155">Quando si verifica un evento per cui è registrata un'applicazione, viene avviata l'applicazione e le informazioni sull'evento vengono trasmesse all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80558-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="80558-156">Usare il metodo [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) per recuperare un puntatore a un oggetto enumeratore per le proprietà di registrazione eventi.</span><span class="sxs-lookup"><span data-stu-id="80558-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="80558-157">Usare il metodo **IWiaDevMgr2:: RegisterEventCallbackProgram** per la compatibilità con le versioni precedenti con le applicazioni non scritte per l'architettura WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="80558-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="80558-158">Usare le interfacce Component Object Model (COM) fornite dall'architettura WIA 2,0 per le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="80558-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="80558-159">In particolare, chiamare [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) per registrare una nuova applicazione per gli eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80558-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="80558-160">In genere, questo metodo viene chiamato da un programma di installazione o da uno script.</span><span class="sxs-lookup"><span data-stu-id="80558-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="80558-161">Il programma o lo script di installazione registra l'applicazione per la ricezione di eventi del dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="80558-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="80558-162">Quando si verifica l'evento, l'applicazione viene avviata dal sistema di runtime WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="80558-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="80558-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80558-163">Requirements</span></span>



| <span data-ttu-id="80558-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="80558-164">Requirement</span></span> | <span data-ttu-id="80558-165">Valore</span><span class="sxs-lookup"><span data-stu-id="80558-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="80558-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80558-166">Minimum supported client</span></span><br/> | <span data-ttu-id="80558-167">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80558-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80558-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80558-168">Minimum supported server</span></span><br/> | <span data-ttu-id="80558-169">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80558-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80558-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80558-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="80558-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="80558-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




