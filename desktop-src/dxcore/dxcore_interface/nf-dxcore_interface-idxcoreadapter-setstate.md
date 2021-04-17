---
title: IDXCoreAdapter::SetState
description: Imposta lo stato dell'elemento specificato nell'adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300214"
---
# <a name="idxcoreadaptersetstate-method"></a>Metodo IDXCoreAdapter:: sestate

Imposta lo stato dell'elemento specificato nell'adapter. Prima di chiamare **lo stato** per un tipo di proprietà, chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.

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

Tipo di elemento di stato nell'adapter di cui si desidera impostare lo stato. Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Tipo: **size_t**

Dimensioni, in byte, del buffer dei dettagli sullo stato di input che è possibile allocare e fornire in *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Tipo: **void const \***

Puntatore facoltativo a un buffer di dettagli dello stato di input costante allocato nell'applicazione, contenente tutte le informazioni sulla richiesta richieste per il tipo di stato specificato in *stato*. Per ulteriori informazioni su qualsiasi requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputdatasize"></a>inputDataSize

Tipo: **size_t**

Dimensione, in byte, del buffer di input allocato e fornito in *inputData*.

### <a name="inputdata-in"></a>inputData [in]

Tipo: **void \***

Puntatore a un buffer di input allocato nell'applicazione, che contiene le informazioni sullo stato da impostare per l'elemento di stato il cui tipo è *stato* specificato nello stato. Per ulteriori informazioni sul requisito del buffer di input per un determinato tipo di stato, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Lo stato dell'adapter non è più valido.|
|DXGI_ERROR_INVALID_CALL|Il tipo di stato specificato nello *stato* non è riconosciuto dal sistema operativo. Chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di stato specificato in *state* non è supportato dall'adapter. Chiamare [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) per verificare che l'impostazione del tipo di stato sia disponibile per l'adapter e il sistema operativo.|
|E_INVALIDARG|Viene fornita una dimensione del buffer insufficiente per *inputData* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|
|E_POINTER|`nullptr` è stato specificato per *inputData* (o per *inputStateDetails* in cui è necessario un buffer dei dettagli dello stato di input).|

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)