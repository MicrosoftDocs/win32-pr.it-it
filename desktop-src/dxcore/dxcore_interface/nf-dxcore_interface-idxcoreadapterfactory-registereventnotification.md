---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Esegue la registrazione per ricevere notifiche di condizioni specifiche da un elenco di adapter o adapter di DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3643fbb01fc955049c297a577f18d4d276e73f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473843"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>Metodo IDXCoreAdapterFactory:: RegisterEventNotification

Esegue la registrazione per ricevere notifiche di condizioni specifiche da un elenco di adapter o adapter di DXCore. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Oggetto DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) le cui notifiche si stanno sottoscrivendo.

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo di notifica per cui si sta effettuando la registrazione. Per informazioni sui tipi validi con i tipi di oggetti, vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="callbackfunction-in"></a>callbackFunction [in]

Tipo: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Puntatore a una funzione di callback (implementata dall'applicazione), che viene chiamata dall'oggetto DXCore per gli eventi di notifica. Per la firma della funzione, vedere [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Tipo: **void \***

Puntatore facoltativo a un oggetto contenente informazioni sul contesto. Questo oggetto viene passato alla funzione di callback quando viene generata la notifica.

### <a name="eventcookie-out"></a>eventCookie [out]

Tipo: **uint32_t \***

Puntatore a un valore **uint32_t** . In caso di esito positivo, la funzione dereferenzia il puntatore e imposta il valore su un valore di cookie diverso da zero che rappresenta la registrazione. Utilizzare questo valore del cookie per annullare la registrazione dalla notifica chiamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Vedere la **sezione Osservazioni**.

Se ha esito negativo, la funzione dereferenzia il puntatore e imposta il valore su zero, che rappresenta un valore di cookie non valido.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|*NotificationType* non è supportato dal sistema operativo.|
|E_INVALIDARG|`nullptr` è stato specificato per *dxCoreObject* o se è stata specificata una combinazione di *NotificationType* e *dxCoreObject* non valida.|
|E_POINTER|`nullptr` è stato specificato per *callbackFunction* o *eventCookie*.|

## <a name="remarks"></a>Commenti

Usare **RegisterEventNotification** per registrare gli eventi generati dalle interfacce [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) e [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) . Questi tipi di notifica sono supportati.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|*DxCoreObject* supportati|Note|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indica che l'elenco degli adapter che soddisfano i criteri di filtro è stato modificato. Se l'elenco degli adapter non è aggiornato al momento della registrazione, il callback viene immediatamente chiamato. Questo callback viene eseguito al massimo una volta per ogni registrazione.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indica che l'adapter non è più valido. Se l'adapter non è valido al momento della registrazione, il callback viene immediatamente chiamato.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indica che si è verificato un evento di budget della memoria e che è necessario chiamare [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) per valutare lo stato del budget di memoria corrente. Al momento della registrazione, si verificherà sempre un callback iniziale per consentire l'esecuzione di query sullo stato iniziale.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indica che è necessario valutare nuovamente lo stato della sessione di crittografia corrente. ad esempio, chiamando [ID3D11VideoContext1:: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) per determinare l'effetto del teardown hardware per una specifica interfaccia [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) . Al momento della registrazione, si verificherà sempre un callback iniziale per consentire l'esecuzione di query sullo stato iniziale.|

Una chiamata alla funzione fornita in *callbackFunction* viene eseguita in modo asincrono in un thread in background da DXCore quando si verifica l'evento rilevato. Non viene garantita alcuna garanzia per quanto riguarda l'ordinamento o la tempistica dei callback &mdash; , più callback possono verificarsi in qualsiasi ordine o anche simultaneamente. È anche possibile che il callback venga richiamato prima del completamento di **RegisterEventNotification** . In tal caso, DXCore garantisce che *eventCookie* sia impostato prima della chiamata al callback. Più callback per una registrazione specifica verranno serializzati nell'ordine.

I callback possono verificarsi in qualsiasi momento fino a quando non si chiama [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)e viene completato. I callback si verificano nei propri thread ed è possibile effettuare chiamate all'API DXCore su tali thread, incluso **UnregisterEventNotification**. Tuttavia, non è necessario rilasciare l'ultimo riferimento a *dxCoreObject* in questo thread.

> [!IMPORTANT]
> Prima di eliminare l'oggetto DXCore rappresentato dall'argomento *dxCoreObject* passato a **RegisterEventNotification**, è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Se non si esegue questa operazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)