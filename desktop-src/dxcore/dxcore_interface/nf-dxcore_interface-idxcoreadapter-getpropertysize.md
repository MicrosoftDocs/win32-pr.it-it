---
title: IDXCoreAdapter::GetPropertySize
description: Per una proprietà dell'adapter specificata, recupera la dimensione del buffer, in byte, necessaria per una chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299974"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Metodo IDXCoreAdapter:: GetPropertySize

Per una proprietà dell'adapter specificata, recupera la dimensione del buffer, in byte, necessaria per una chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Prima di chiamare **GetPropertySize** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="property"></a>proprietà

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo della proprietà le cui dimensioni, in byte, si desidera recuperare.

### <a name="buffersize-out"></a>bufferSize [out]

Tipo: **size_t \***

Puntatore a un valore **size_t** . La funzione dereferenzia il puntatore e imposta il valore sulla dimensione, in byte, del buffer di output che è necessario allocare e passare come argomento *PropertyData* nella chiamata a [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|Il tipo di proprietà specificato nella *Proprietà* non è riconosciuto dal sistema operativo. Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di proprietà specificato nella *Proprietà* non è supportato dall'adapter. Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|E_POINTER|`nullptr` fornito per *bufferSize*.|

## <a name="remarks"></a>Commenti

È possibile chiamare **GetPropertySize** su un adapter non più valido &mdash; . la funzione non avrà esito negativo.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)