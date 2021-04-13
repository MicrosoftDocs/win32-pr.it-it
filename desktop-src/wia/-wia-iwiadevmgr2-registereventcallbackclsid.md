---
description: "Il metodo IWiaDevMgr2:: RegisterEventCallbackCLSID registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione."
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackCLSID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527073"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="8a868-103">Metodo IWiaDevMgr2:: RegisterEventCallbackCLSID</span><span class="sxs-lookup"><span data-stu-id="8a868-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="8a868-104">Il metodo **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8a868-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a868-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a868-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="8a868-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a868-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8a868-108">Type: **LONG**</span></span>

<span data-ttu-id="8a868-109">Specifica i flag di registrazione.</span><span class="sxs-lookup"><span data-stu-id="8a868-109">Specifies registration flags.</span></span> <span data-ttu-id="8a868-110">Può essere impostato sui valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a868-110">Can be set to the following values:</span></span>



| <span data-ttu-id="8a868-111">Flag di registrazione</span><span class="sxs-lookup"><span data-stu-id="8a868-111">Registration Flag</span></span>                | <span data-ttu-id="8a868-112">Significato</span><span class="sxs-lookup"><span data-stu-id="8a868-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="8a868-113">\_callback di \_ evento di registro WIA \_</span><span class="sxs-lookup"><span data-stu-id="8a868-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="8a868-114">Eseguire la registrazione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-114">Register for the event.</span></span>                           |
| <span data-ttu-id="8a868-115">\_callback di evento WIA Annulla registrazione \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a868-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="8a868-116">Eliminare la registrazione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="8a868-117">\_ \_ gestore predefinito set \_ WIA</span><span class="sxs-lookup"><span data-stu-id="8a868-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="8a868-118">Impostare l'applicazione come gestore eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8a868-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8a868-119">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-120">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a868-120">Type: **BSTR**</span></span>

<span data-ttu-id="8a868-121">Specifica un identificatore di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a868-121">Specifies a device identifier.</span></span> <span data-ttu-id="8a868-122">Passare **null** per eseguire la registrazione per l'evento in tutti i dispositivi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8a868-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="8a868-123">*pEventGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-124">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="8a868-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="8a868-125">Specifica l'evento per cui si sta registrando l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a868-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="8a868-126">Per un elenco degli eventi standard, vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="8a868-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a868-127">_pClsID \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-128">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="8a868-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="8a868-129">Puntatore all'ID della classe dell'applicazione (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="8a868-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="8a868-130">Il sistema di runtime WIA 2,0 utilizza l'applicazione **CLSID** per avviare l'applicazione quando si verifica un evento per cui è registrata.</span><span class="sxs-lookup"><span data-stu-id="8a868-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="8a868-131">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-132">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a868-132">Type: **BSTR**</span></span>

<span data-ttu-id="8a868-133">Specifica il nome dell'applicazione che registra per l'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="8a868-134">*bstrDescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-135">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a868-135">Type: **BSTR**</span></span>

<span data-ttu-id="8a868-136">Specifica una descrizione di testo dell'applicazione che esegue la registrazione per l'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="8a868-137">*bstrIcon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a868-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a868-138">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a868-138">Type: **BSTR**</span></span>

<span data-ttu-id="8a868-139">Specifica il nome di un file di immagine da utilizzare per l'icona dell'applicazione registrata per l'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a868-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a868-140">Return value</span></span>

<span data-ttu-id="8a868-141">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8a868-141">Type: **HRESULT**</span></span>

<span data-ttu-id="8a868-142">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8a868-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a868-143">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a868-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a868-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a868-144">Remarks</span></span>

<span data-ttu-id="8a868-145">Le applicazioni WIA 2,0 usano questo metodo per eseguire la registrazione in modo da ricevere gli eventi del dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="8a868-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="8a868-146">Dopo la chiamata di **IWiaDevMgr2:: RegisterEventCallbackCLSID** , l'applicazione viene registrata per la ricezione di eventi del dispositivo WIA 2,0 anche se non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8a868-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="8a868-147">Quando si verifica l'evento, il sistema WIA 2,0 determina quale applicazione è registrata per la ricezione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="8a868-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="8a868-148">Usa la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e il CLSID specificato nel parametro *pClsID* per creare un'istanza dell'applicazione, quindi chiama il metodo [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) per trasmettere le informazioni sull'evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a868-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="8a868-149">Un'applicazione può richiamare il metodo [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) per enumerare le informazioni di registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="8a868-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="8a868-150">Se l'applicazione non è un componente Component Object Model registrato (COM) e non è compatibile con l'architettura WIA 2,0, usare il metodo [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per registrare un'applicazione per gli eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a868-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="8a868-151">In un'applicazione multithread non vi è alcuna garanzia che venga restituito il callback della notifica degli eventi sullo stesso thread che ha registrato il callback.</span><span class="sxs-lookup"><span data-stu-id="8a868-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a868-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a868-152">Requirements</span></span>



| <span data-ttu-id="8a868-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a868-153">Requirement</span></span> | <span data-ttu-id="8a868-154">Valore</span><span class="sxs-lookup"><span data-stu-id="8a868-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8a868-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a868-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8a868-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a868-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a868-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a868-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8a868-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a868-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8a868-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a868-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a868-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a868-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
