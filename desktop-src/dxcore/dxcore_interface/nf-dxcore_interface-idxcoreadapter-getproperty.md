---
title: IDXCoreAdapter::GetProperty
description: Recupera il valore della proprietà dell'adattatore specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279401"
---
# <a name="idxcoreadaptergetproperty-method"></a>Metodo IDXCoreAdapter::GetProperty

Recupera il valore della proprietà dell'adattatore specificata. Prima di **chiamare GetProperty** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per questo adapter e il sistema operativo. Anche prima di **chiamare GetProperty,** chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare le dimensioni necessarie del buffer in cui ricevere il valore della proprietà.

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Parametri

### <a name="property"></a>proprietà

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo della proprietà di cui si desidera recuperare il valore. Per altre informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty.](./ne-dxcore_interface-dxcoreadapterproperty.md)

### <a name="buffersize"></a>bufferSize

Tipo: **size_t**

Dimensione, in byte, del buffer di output allocato e fornito in *propertyData.*

### <a name="propertydata-out"></a>propertyData [out]

Tipo: **\* void**

Puntatore a un buffer di output allocato nell'applicazione e che la funzione riempie. Chiamare [GetPropertySize per](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) determinare le dimensioni del buffer *propertyData* per una determinata proprietà dell'adapter.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|Il tipo di proprietà specificato *nella proprietà* non è riconosciuto da questo sistema operativo. Chiamare [IsPropertySupported per](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di proprietà specificato nella *proprietà* non è supportato dall'adapter. Chiamare [IsPropertySupported per](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|E_INVALIDARG|Le dimensioni del buffer specificate in propertyData sono *insufficienti.* Chiamare [GetPropertySize per](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) determinare le dimensioni del buffer *propertyData* per una determinata proprietà dell'adapter.|
|E_POINTER|`nullptr` è stato fornito per *propertyData*.|

## <a name="remarks"></a>Commenti

È possibile chiamare **GetProperty** su un adattatore non più valido per cui la funzione non avrà esito &mdash; negativo. Questa funzione azzera il buffer *propertyData* prima di compilarlo.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)