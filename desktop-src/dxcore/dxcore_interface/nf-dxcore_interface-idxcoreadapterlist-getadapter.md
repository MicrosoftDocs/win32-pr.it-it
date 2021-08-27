---
title: IDXCoreAdapterList::GetAdapter
description: Recupera un adattatore specifico in base all'indice da un oggetto elenco di adattatori DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 96b2973e36c93ca50db273fc28bd0f02cbaf7a48f96e6833af7f14323c7de57d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022131"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>Metodo IDXCoreAdapterList::GetAdapter

Recupera un adattatore specifico in base all'indice da un oggetto elenco di adattatori DXCore. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parametri

### <a name="index"></a>index

Tipo: **uint32_t**

Indice in base zero che identifica un'istanza dell'adattatore all'interno dell'elenco di adattatori DXCore.

### <a name="riid"></a>Riid

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
|DXGI_ERROR_DEVICE_REMOVED|*L'indice* è valido, ma l'adattatore non è più in uno stato valido.|
|E_INVALIDARG|*L'indice specificato* non è valido.|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` è stato fornito per *ppvAdapter*.|

## <a name="remarks"></a>Commenti

Più chiamate che passano un indice che rappresenta lo stesso adattatore restituiscono puntatori a interfaccia identici, anche in elenchi di adattatori diversi. Di conseguenza, è possibile confrontare i puntatori a interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adattatore.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)