---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Annulla la registrazione di una notifica registrata in precedenza per.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399516"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Metodo IDXCoreAdapterFactory:: UnregisterEventNotification

Annulla la registrazione di una notifica registrata in precedenza per. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

Valore del cookie (restituito quando è stato chiamato [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) che rappresenta una registrazione precedente a cui si desidera annullare la registrazione.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|Il valore di *eventCookie* non è un cookie valido che rappresenta una registrazione precedente.|

## <a name="remarks"></a>Commenti

**UnregisterEventNotification** restituisce solo dopo il completamento di tutti i callback in sospeso/in corso per la registrazione. DXCore garantisce che non si verificheranno nuovi callback per questa registrazione dopo che è stato restituito **UnregisterEventNotification** . Tuttavia, per evitare un deadlock, se si chiama **UnregisterEventNotification** dall'interno del callback, **UnregisterEventNotification** non attende il completamento del callback attivo.

> [!IMPORTANT]
> Prima di eliminare l'oggetto DXCore rappresentato dall'argomento *dxCoreObject* passato a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando **UnregisterEventNotification**. Se non si esegue questa operazione, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

Una volta annullata la registrazione di un valore di cookie, tale valore sarà quindi idoneo per essere restituito da una registrazione successiva

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)