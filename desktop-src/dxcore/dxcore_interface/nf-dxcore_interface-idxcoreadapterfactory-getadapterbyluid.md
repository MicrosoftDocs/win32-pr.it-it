---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d8f72aba23b9a1f57094b39e5afba3740f8749348c6a2da6a8753f72a7a0e6ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787053"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>Metodo IDXCoreAdapterFactory::GetAdapterByLuid

Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parametri

### <a name="adapterluid"></a>adapterLUID

Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

Valore univoco locale che identifica l'istanza dell'adapter.

### <a name="riid-in"></a>riid [in]

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire in *ppvAdapter.* Si tratta dell'identificatore di interfaccia (IID) di [IDXCoreAdapter.](./nn-dxcore_interface-idxcoreadapter.md)

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Tipo: **\* \* void**

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel *parametro riid.* Al completamento della restituzione, *\* ppvAdapter* (l'indirizzo dereferenziato) contiene un puntatore all'adapter DXCore creato.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md).

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L'adapter LUID passato in *adapterLUID* viene riconosciuto, ma l'adapter non è più in uno stato valido.|
|E_INVALIDARG|Non è disponibile alcun LUID dell'adapter di questo tipo perché il valore passato in *adapterLUID* è disponibile tramite DXCore.|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` è stato fornito per *ppvAdapter*.|

## <a name="remarks"></a>Commenti

Più chiamate che passano lo [stesso LUID](/windows/win32/api/winnt/ns-winnt-luid) restituiscono puntatori a interfaccia identici. Di conseguenza, è possibile confrontare i puntatori a interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adattatore.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)