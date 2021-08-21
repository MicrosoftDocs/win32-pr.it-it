---
description: Funzione proxy per il metodo GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: IWICMetadataQueryReader_GetEnumerator_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f93f064705306ba32dccf1263e80d44b7adfb3ed59e00e5b22b9cf0148e4d6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033597"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a>Funzione proxy GetEnumerator IWICMetadataQueryReader \_ \_

Funzione proxy per il [**metodo GetEnumerator.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Puntatore a [**questo oggetto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)

</dd> <dt>

*ppIEnumString* \[ Cambio\]
</dt> <dd>

Tipo: **IEnumString \* \***

Puntatore che riceve un puntatore a un enumeratore di metadati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




