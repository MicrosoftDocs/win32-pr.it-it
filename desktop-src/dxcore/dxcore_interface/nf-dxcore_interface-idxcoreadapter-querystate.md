---
title: IDXCoreAdapter::QueryState
description: Recupera lo stato corrente dell'elemento specificato nell'adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300215"
---
# <a name="idxcoreadapterquerystate-method"></a>Metodo IDXCoreAdapter:: QueryState

Recupera lo stato corrente dell'elemento specificato nell'adapter. Prima di chiamare **QueryState** per un tipo di proprietà, chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per l'adapter e il sistema operativo.

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato nell'adapter di cui si desidera recuperare lo stato. Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Dimensioni, in byte, del buffer dei dettagli sullo stato di input che è possibile allocare e fornire in *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Puntatore facoltativo a un buffer di dettagli dello stato di input costante allocato nell'applicazione, contenente tutte le informazioni sulla richiesta richieste per il tipo di stato specificato in *stato*. Per ulteriori informazioni su qualsiasi requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="outputbuffersize"></a>outputBufferSize

Tipo: **size_t**

Dimensione, in byte, del buffer di output allocato e fornito in *outputBuffer*.

### <a name="outputbuffer-out"></a>outputBuffer [out]

Tipo: **void \***

Puntatore a un buffer di output allocato nell'applicazione e che la funzione compila. Per altre informazioni sul requisito del buffer di output per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Lo stato dell'adapter non è più valido.|
|DXGI_ERROR_INVALID_CALL|Il tipo di stato specificato nello *stato* non è riconosciuto dal sistema operativo. Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di stato specificato in *state* non è supportato dall'adapter. Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di una query sul tipo di stato sia disponibile per questo adapter e il sistema operativo.|
|E_INVALIDARG|Viene fornita una dimensione del buffer insufficiente per *outputBuffer* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|
|E_POINTER|`nullptr` è stato specificato per *outputBuffer* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|

## <a name="remarks"></a>Commenti

Vedere [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) per altre informazioni su ogni tipo di stato dell'adapter e sugli input e sugli output usati. Questa funzione azzera il buffer *outputBuffer* prima di riempirlo.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)