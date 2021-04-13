---
title: IDXCoreAdapter::GetProperty
description: Recupera il valore della proprietà dell'adapter specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338975"
---
# <a name="idxcoreadaptergetproperty-method"></a>Metodo IDXCoreAdapter:: GetProperty

Recupera il valore della proprietà dell'adapter specificata. Prima di chiamare **GetProperty** per un tipo di proprietà, chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo. Inoltre, prima di chiamare **GetProperty**, chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare la dimensione necessaria del buffer in cui ricevere il valore della proprietà.

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

Tipo della proprietà di cui si desidera recuperare il valore. Per ulteriori informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .

### <a name="buffersize"></a>bufferSize

Tipo: **size_t**

Dimensione, in byte, del buffer di output allocato e fornito in *PropertyData*.

### <a name="propertydata-out"></a>propertyData [out]

Tipo: **void \***

Puntatore a un buffer di output allocato nell'applicazione e che la funzione compila. Chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare le dimensioni del buffer *PropertyData* per una determinata proprietà dell'adapter.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|DXGI_ERROR_INVALID_CALL|Il tipo di proprietà specificato nella *Proprietà* non è riconosciuto dal sistema operativo. Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|DXGI_ERROR_UNSUPPORTED|Il tipo di proprietà specificato nella *Proprietà* non è supportato dall'adapter. Chiamare [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) per verificare che il tipo di proprietà sia disponibile per l'adapter e il sistema operativo.|
|E_INVALIDARG|In *PropertyData* è disponibile una dimensione del buffer insufficiente. Chiamare [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) per determinare le dimensioni del buffer *PropertyData* per una determinata proprietà dell'adapter.|
|E_POINTER|`nullptr` fornito per *PropertyData*.|

## <a name="remarks"></a>Commenti

È possibile chiamare **GetProperty** su un adapter che non è più valido &mdash; . la funzione non avrà esito negativo come conseguenza. Questa funzione azzera il buffer *PropertyData* prima di riempirlo.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)