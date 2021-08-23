---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Registra per ricevere notifiche di condizioni specifiche da un elenco di adapter O adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b97b51f7c4359526317647b62241e37063243a56f45014c28ba2f2cd897706ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042899"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>Metodo IDXCoreAdapterFactory::RegisterEventNotification

Registra per ricevere notifiche di condizioni specifiche da un elenco di adapter O adapter DXCore. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

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

Oggetto DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) di cui si stanno sottoscrivendo le notifiche.

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo di notifica per cui si sta registrando. Vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) per informazioni sui tipi validi con quali tipi di oggetti.

### <a name="callbackfunction-in"></a>callbackFunction [in]

Tipo: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Puntatore a una funzione di callback (implementata dall'applicazione), chiamata dall'oggetto DXCore per gli eventi di notifica. Per la firma della funzione, [vedere](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)PFN_DXCORE_NOTIFICATION_CALLBACK .

### <a name="callbackcontext-in"></a>callbackContext [in]

Tipo: **\* void**

Puntatore facoltativo a un oggetto contenente informazioni di contesto. Questo oggetto viene passato alla funzione di callback quando viene generata la notifica.

### <a name="eventcookie-out"></a>eventCookie [out]

Tipo: **uint32_t \***

Puntatore a un **uint32_t** valore. In caso di esito positivo, la funzione dereferenzia il puntatore e imposta il valore su un valore di cookie diverso da zero che rappresenta la registrazione. Usare questo valore del cookie per annullare la registrazione dalla notifica chiamando [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Vedere **Note**.

In caso di esito negativo, la funzione dereferenzia il puntatore e imposta il valore su zero, che rappresenta un valore di cookie non valido.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|*notificationType* non è supportato dal sistema operativo.|
|E_INVALIDARG|`nullptr` è stato fornito *per dxCoreObject* o se è stata specificata una *combinazione notificationType* e *dxCoreObject* non valida.|
|E_POINTER|`nullptr` è stato fornito per *callbackFunction* o *eventCookie*.|

## <a name="remarks"></a>Commenti

Usare **RegisterEventNotification per** registrarsi per gli eventi generati dalle [interfacce IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) e [IDXCoreAdapter.](./nn-dxcore_interface-idxcoreadapter.md) Questi tipi di notifica sono supportati.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|*DxCoreObject supportato*|Note|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indica che l'elenco di schede che soddisfano i criteri di filtro è stato modificato. Se l'elenco di adapter non è disponibile al momento della registrazione, il callback viene chiamato immediatamente. Questo callback si verifica al massimo una volta per ogni registrazione.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indica che l'adapter non è più valido. Se l'adapter non è valido in fase di registrazione, il callback viene chiamato immediatamente.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indica che si è verificato un evento di budget della memoria e che è necessario chiamare [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState::AdapterMemoryBudget)](./ne-dxcore_interface-dxcoreadapterstate.md)per valutare lo stato corrente del budget di memoria. Al momento della registrazione, verrà sempre eseguito un callback iniziale per consentire di eseguire query sullo stato iniziale.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indica che è necessario valutare nuovamente lo stato della sessione di crittografia corrente. ad esempio chiamando [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) per determinare l'impatto della rimozione dell'hardware per [un'interfaccia ID3D11CryptoSession specifica.](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) Al momento della registrazione, verrà sempre eseguito un callback iniziale per consentire di eseguire query sullo stato iniziale.|

Una chiamata alla funzione specificata in *callbackFunction* viene eseguita in modo asincrono in un thread in background da DXCore quando si verifica l'evento rilevato. Non viene garantita l'ordinamento o la tempistica dei callback, è possibile che più callback si verifichino in qualsiasi &mdash; ordine o anche contemporaneamente. È anche possibile che il callback venga richiamato prima del **completamento di RegisterEventNotification.** In tal caso, DXCore garantisce che *eventCookie* sia impostato prima che venga chiamato il callback. Più callback per una registrazione specifica verranno serializzati nell'ordine indicato.

I callback possono verificarsi in qualsiasi momento fino a quando non si [chiama UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)e viene completato. I callback si verificano nei propri thread ed è possibile effettuare chiamate all'API DXCore su tali thread, incluso **UnregisterEventNotification**. Tuttavia, non è necessario rilasciare l'ultimo riferimento a *dxCoreObject* in questo thread.

> [!IMPORTANT]
> Prima di eliminare l'oggetto DXCore rappresentato dall'argomento *dxCoreObject* passato a **RegisterEventNotification,** è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). In caso contrario, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)