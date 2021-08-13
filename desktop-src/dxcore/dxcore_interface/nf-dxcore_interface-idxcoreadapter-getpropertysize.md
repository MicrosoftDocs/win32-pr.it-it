---
title: IDXCoreAdapter::GetPropertySize
description: Per una proprietà dell'adattatore specificata, recupera le dimensioni del buffer, in byte, necessarie per una chiamata a [GetProperty.](./nf-dxcore_interface-idxcoreadapter-getproperty.md)
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 525e2657ab7af5fa6f7cee4f527b74604d2674dbc67da232dd6501ddc45b0291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279253"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Metodo IDXCoreAdapter::GetPropertySize

Per una proprietà dell'adattatore specificata, recupera le dimensioni del buffer, in byte, necessarie per una chiamata a [GetProperty.](./nf-dxcore_interface-idxcoreadapter-getproperty.md) Prima di **chiamare GetPropertySize** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per questo adattatore e sistema operativo.

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="property"></a>proprietà

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo della proprietà di cui si desidera recuperare le dimensioni, in byte.

### <a name="buffersize-out"></a>bufferSize [out]

Tipo: **size_t \***

Puntatore a un **size_t** specificato. La funzione dereferenzia il puntatore e imposta il valore sulla dimensione, in byte, del buffer di output che è necessario allocare e passare come argomento *propertyData* nella chiamata a [GetProperty.](./nf-dxcore_interface-idxcoreadapter-getproperty.md)

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md).

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|Il tipo di proprietà specificato *nella proprietà* non è riconosciuto da questo sistema operativo. Chiamare [IsPropertySupported per](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) verificare che il tipo di proprietà sia disponibile per questa scheda e sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di proprietà specificato nella *proprietà* non è supportato dall'adattatore. Chiamare [IsPropertySupported per](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) verificare che il tipo di proprietà sia disponibile per questa scheda e sistema operativo.|
|E_POINTER|`nullptr`è stato fornito per *bufferSize.*|

## <a name="remarks"></a>Commenti

È possibile chiamare **GetPropertySize** su un adapter che non è più valido. La &mdash; funzione non avrà esito negativo.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)