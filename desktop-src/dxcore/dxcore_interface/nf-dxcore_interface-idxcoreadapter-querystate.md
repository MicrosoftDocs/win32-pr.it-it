---
title: IDXCoreAdapter::QueryState
description: Recupera lo stato corrente dell'elemento specificato nell'adattatore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2e5c585c249141c1491ddf36ee798d8b11148425026e9011bd0653169f998fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117721"
---
# <a name="idxcoreadapterquerystate-method"></a>Metodo IDXCoreAdapter::QueryState

Recupera lo stato corrente dell'elemento specificato nell'adattatore. Prima di **chiamare QueryState** per un tipo di proprietà, chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che sia disponibile l'esecuzione di query sul tipo di stato per questo adapter e il sistema operativo.

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

Tipo di elemento di stato nell'adapter di cui si vuole recuperare lo stato. Per altre informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Dimensione, in byte, del buffer dei dettagli dello stato di input allocato (facoltativamente) e fornito in *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void \* const**

Puntatore facoltativo a un buffer dei dettagli dello stato di input costante allocato nell'applicazione, contenente le informazioni sulla richiesta necessarie per il tipo di stato specificato nello *stato*. Per altre informazioni sui requisiti del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="outputbuffersize"></a>outputBufferSize

Tipo: **size_t**

Dimensione, in byte, del buffer di output allocato e fornito in *outputBuffer*.

### <a name="outputbuffer-out"></a>outputBuffer [out]

Tipo: **\* void**

Puntatore a un buffer di output allocato nell'applicazione e che la funzione riempie. Per altre informazioni sul requisito del buffer di output per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L'adapter non è più in uno stato valido.|
|DXGI_ERROR_INVALID_CALL|Il tipo di stato specificato *nello stato* non è riconosciuto da questo sistema operativo. Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di query sul tipo di stato sia disponibile per questa scheda e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di stato specificato *nello stato* non è supportato dall'adapter. Chiamare [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) per verificare che l'esecuzione di query sul tipo di stato sia disponibile per questa scheda e il sistema operativo.|
|E_INVALIDARG|Dimensioni del buffer insufficienti per *outputBuffer* (o *per inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|
|E_POINTER|`nullptr` è stato fornito *per outputBuffer* (o *per inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|

## <a name="remarks"></a>Commenti

Per altre informazioni su ogni tipo di stato dell'adapter e sugli input e gli output usati, vedere [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md) Questa funzione azzera il buffer *outputBuffer* prima di compilarlo.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)