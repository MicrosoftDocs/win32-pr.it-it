---
title: IDXCoreAdapterList::GetFactory
description: Recupera un puntatore a [interfaccia IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adapter DXCore. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 97ae5ef0ba321dafaabf1813d943b738f5af4c586050b91712bf9ad93005cb35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094581"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>Metodo IDXCoreAdapterList::GetFactory

Recupera un puntatore a [interfaccia IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adapter DXCore. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parametri

### <a name="riid"></a>Riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si vuole restituire in *ppvFactory.* Si prevede che sia l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory.](./nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel *parametro riid.* Al completamento della restituzione, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore all'oggetto factory dell'adapter DXCore esistente. Prima della restituzione, la funzione incrementa il conteggio dei riferimenti [sull'interfaccia IDXCoreAdapterFactory dell'oggetto](./nn-dxcore_interface-idxcoreadapterfactory.md) factory.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` è stato fornito per *ppvFactory*.|

## <a name="remarks"></a>Commenti

Per la durata dell'esistenza di un riferimento in [un'interfaccia IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [un'interfaccia IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) le chiamate aggiuntive a [DXCoreCreateAdapterFactory,](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md) [IDXCoreAdapterList::GetFactory]()o [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
