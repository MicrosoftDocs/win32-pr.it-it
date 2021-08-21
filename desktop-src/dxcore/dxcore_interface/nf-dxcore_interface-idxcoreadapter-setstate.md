---
title: IDXCoreAdapter::SetState
description: Imposta lo stato dell'elemento specificato nell'adattatore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c80ca670be26ffdcefa5e89cee079d2225d204ee97e99e41f69686300a46230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042909"
---
# <a name="idxcoreadaptersetstate-method"></a>Metodo IDXCoreAdapter::SetState

Imposta lo stato dell'elemento specificato nell'adattatore. Prima di **chiamare SetState** per un tipo di proprietà, chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per questo adapter e il sistema operativo.

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato nell'adapter di cui si desidera impostare lo stato. Per altre informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Dimensione, in byte, del buffer dei dettagli dello stato di input allocato (facoltativamente) e fornito in *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void \* const**

Puntatore facoltativo a un buffer dei dettagli dello stato di input costante allocato nell'applicazione, contenente le informazioni sulla richiesta necessarie per il tipo di stato specificato nello *stato*. Per altre informazioni sui requisiti del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputdatasize"></a>inputDataSize

Tipo: **size_t**

Dimensione, in byte, del buffer di input allocato e fornito in *inputData*.

### <a name="inputdata-in"></a>inputData [in]

Tipo: **\* void**

Puntatore a un buffer di input allocato nell'applicazione, contenente le informazioni sullo stato da impostare per l'elemento di stato di cui si specifica il tipo nello *stato*. Per altre informazioni sul requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L'adapter non è più in uno stato valido.|
|DXGI_ERROR_INVALID_CALL|Il tipo di stato specificato *nello stato* non è riconosciuto da questo sistema operativo. Chiamare [IsSetStateSupported per](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) verificare che l'impostazione del tipo di stato sia disponibile per questa scheda e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di stato specificato *nello stato* non è supportato dall'adapter. Chiamare [IsSetStateSupported per](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) verificare che l'impostazione del tipo di stato sia disponibile per questa scheda e il sistema operativo.|
|E_INVALIDARG|Dimensioni del buffer insufficienti per *inputData* (o *per inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|
|E_POINTER|`nullptr` è stato fornito *per inputData* (o *per inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)