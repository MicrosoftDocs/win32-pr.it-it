---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Annulla la registrazione da una notifica per cui è stata precedentemente registrata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 64fb54226f1fad0d1d36f8f4260c9c9172b105dc6239ea5cb805c32b57a938ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278882"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Metodo IDXCoreAdapterFactory::UnregisterEventNotification

Annulla la registrazione da una notifica per cui è stata precedentemente registrata. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

Valore del cookie (restituito quando si chiama [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) che rappresenta una registrazione precedente per cui si vuole annullare la registrazione.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|E_INVALIDARG|Il valore di *eventCookie* non è un cookie valido che rappresenta una registrazione precedente.|

## <a name="remarks"></a>Commenti

**UnregisterEventNotification** restituisce solo dopo il completamento di tutti i callback in sospeso/in corso per questa registrazione. DXCore garantisce che non verranno eseguiti nuovi callback per questa registrazione dopo la **restituita unregisterEventNotification.** Tuttavia, per evitare un deadlock, se si chiama **UnregisterEventNotification** dall'interno del callback, **UnregisterEventNotification** non attende il completamento del callback attivo.

> [!IMPORTANT]
> Prima di eliminare l'oggetto DXCore rappresentato dall'argomento *dxCoreObject* passato [a IDXCoreAdapterFactory::RegisterEventNotification,](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)è necessario usare il valore del cookie per annullare la registrazione dell'oggetto dalle notifiche chiamando **UnregisterEventNotification**. In caso contrario, viene generata un'eccezione irreversibile quando viene rilevata la situazione.

Dopo aver annullato la registrazione di un valore del cookie, tale valore è idoneo per essere restituito da una registrazione successiva

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)