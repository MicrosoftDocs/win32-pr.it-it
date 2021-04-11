---
title: Metodo IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica al modulo di reindirizzamento del dispositivo del Desktop remoto controllo ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa \_ le notifiche di WM DEVICECHANGE al controllo.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
- Metodo NotifyRedirectDeviceChange Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, metodo NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964883"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="a0a56-115">Metodo IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange</span><span class="sxs-lookup"><span data-stu-id="a0a56-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="a0a56-116">Notifica al modulo di reindirizzamento del dispositivo del Desktop remoto controllo ActiveX che si è verificata una modifica del dispositivo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a0a56-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="a0a56-117">Questo metodo passa le notifiche di [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al controllo.</span><span class="sxs-lookup"><span data-stu-id="a0a56-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a56-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0a56-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="a0a56-119">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0a56-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-120">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0a56-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-121">Specifica l'evento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a56-121">Specifies the device event.</span></span> <span data-ttu-id="a0a56-122">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0a56-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="a0a56-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**\_CONFIGCHANGECANCELED DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-124">Una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="a0a56-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="a0a56-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**\_CONFIGCHANGED DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-126">La configurazione corrente è cambiata a causa di un ancoraggio o di Undock.</span><span class="sxs-lookup"><span data-stu-id="a0a56-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="a0a56-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**\_CUSTOMEVENT DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-128">Si è verificato un evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a0a56-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="a0a56-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**\_DEVICEARRIVAL DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-130">Un dispositivo è stato inserito ed è ora disponibile.</span><span class="sxs-lookup"><span data-stu-id="a0a56-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="a0a56-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**\_DEVICEQUERYREMOVE DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-132">Viene richiesta l'autorizzazione per rimuovere un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a56-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="a0a56-133">Qualsiasi applicazione può negare questa richiesta e annullare la rimozione.</span><span class="sxs-lookup"><span data-stu-id="a0a56-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="a0a56-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**\_DEVICEQUERYREMOVEFAILED DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-135">Una richiesta di rimozione di un dispositivo è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="a0a56-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="a0a56-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**\_DEVICEREMOVECOMPLETE DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-137">Un dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="a0a56-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="a0a56-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**\_DEVICEREMOVEPENDING DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-139">Un dispositivo sta per essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="a0a56-139">A device is about to be removed.</span></span> <span data-ttu-id="a0a56-140">Non è possibile negare la rimozione.</span><span class="sxs-lookup"><span data-stu-id="a0a56-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="a0a56-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**\_DEVICETYPESPECIFIC DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-142">Si è verificato un evento specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a56-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="a0a56-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**\_DEVNODE DBT \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="a0a56-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-144">Un dispositivo è stato aggiunto o rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a0a56-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="a0a56-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**\_QUERYCHANGECONFIG DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-146">Viene richiesta l'autorizzazione per modificare la configurazione corrente (dock o Undock).</span><span class="sxs-lookup"><span data-stu-id="a0a56-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="a0a56-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**\_USERDEFINED DBT**</span><span class="sxs-lookup"><span data-stu-id="a0a56-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="a0a56-148">Il significato di questo messaggio è definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a0a56-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0a56-149">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0a56-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-150">Puntatore a una struttura che contiene dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="a0a56-151">Il formato dipende dal valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a0a56-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="a0a56-152">Per ulteriori informazioni, vedere la documentazione relativa a ogni evento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="a0a56-153">Per altre informazioni, vedere [tipi di eventi del dispositivo](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="a0a56-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a56-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0a56-154">Return value</span></span>

<span data-ttu-id="a0a56-155">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a56-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0a56-156">Remarks</span></span>

<span data-ttu-id="a0a56-157">Un'applicazione contenitore che consente l'aggiunta o la rimozione dinamica dei dispositivi deve elaborare il messaggio [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) nella finestra di primo livello e trasmettere il messaggio al controllo usando il metodo **NotifyRedirectDeviceChange** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="a0a56-158">Un esempio di una modifica dinamica del dispositivo si verifica quando viene aggiunta o rimossa un'unità disco reindirizzata mentre il sistema è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a0a56-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="a0a56-159">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a0a56-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a56-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0a56-160">Requirements</span></span>



| <span data-ttu-id="a0a56-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a56-161">Requirement</span></span> | <span data-ttu-id="a0a56-162">Valore</span><span class="sxs-lookup"><span data-stu-id="a0a56-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a56-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0a56-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a56-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0a56-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="a0a56-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0a56-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a56-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a56-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="a0a56-167">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a0a56-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0a56-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="a0a56-169">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a56-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a56-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="a0a56-171">IID</span><span class="sxs-lookup"><span data-stu-id="a0a56-171">IID</span></span><br/>                      | <span data-ttu-id="a0a56-172">IID \_ IMsRdpClientNonScriptable è definito come 2f079c4c-87B2-4afd-97AB-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="a0a56-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0a56-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0a56-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a56-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="a0a56-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="a0a56-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a0a56-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="a0a56-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a0a56-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a0a56-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a0a56-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a0a56-178">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a0a56-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

