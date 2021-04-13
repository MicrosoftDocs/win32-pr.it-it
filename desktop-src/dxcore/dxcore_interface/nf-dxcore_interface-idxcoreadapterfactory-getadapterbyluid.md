---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399450"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>Metodo IDXCoreAdapterFactory:: GetAdapterByLuid

Recupera l'oggetto adattatore DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) per un LUID specificato, se disponibile. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

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

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapter*. Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Tipo: **void \* \***

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* . In caso di esito positivo, *\* ppvAdapter* (l'indirizzo dereferenziato) contiene un puntatore alla scheda DXCore creata.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L'adapter LUID passato in *adapterLUID* è riconosciuto, ma lo stato dell'adapter non è più valido.|
|E_INVALIDARG|Nessun adapter di questo tipo LUID come il valore passato in *adapterLUID* è disponibile tramite dxcore.|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` fornito per *ppvAdapter*.|

## <a name="remarks"></a>Commenti

Più chiamate che passano lo stesso [LUID](/windows/win32/api/winnt/ns-winnt-luid) restituiscono puntatori di interfaccia identici. Di conseguenza, è possibile confrontare i puntatori all'interfaccia per determinare se più puntatori fanno riferimento allo stesso oggetto adapter.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)