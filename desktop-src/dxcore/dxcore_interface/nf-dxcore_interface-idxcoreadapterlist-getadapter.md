---
title: IDXCoreAdapterList::GetAdapter
description: Recupera un adapter specifico in base all'indice da un oggetto elenco di adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047171"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>Metodo IDXCoreAdapterList:: GetAdapter

Recupera un adapter specifico in base all'indice da un oggetto elenco di adapter DXCore. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

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

### <a name="index"></a>indice

Tipo: **uint32_t**

Indice in base zero, che identifica un'istanza dell'adapter all'interno dell'elenco di adapter DXCore.

### <a name="riid"></a>riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapter*. Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Tipo: **void \* \***

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* . In caso di esito positivo, *\* ppvAdapter* (l'indirizzo dereferenziato) contiene un puntatore alla scheda DXCore creata.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L' *Indice* è valido, ma lo stato dell'adapter non è più valido.|
|E_INVALIDARG|L' *Indice* specificato non è valido.|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` fornito per *ppvAdapter*.|

## <a name="remarks"></a>Commenti

Più chiamate che passano un indice che rappresenta lo stesso adapter restituiscono puntatori di interfaccia identici, anche in diversi elenchi di adapter. Di conseguenza, è possibile confrontare i puntatori all'interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adapter.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)