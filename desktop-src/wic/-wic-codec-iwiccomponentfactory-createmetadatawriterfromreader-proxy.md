---
description: Funzione proxy per il metodo CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: Funzione IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882446"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a>IWICComponentFactory \_ CreateMetadataWriterFromReader- \_ funzione proxy

Funzione proxy per il metodo [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _

Puntatore a questo oggetto [_ *IWICComponentFactory* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .

</dd> <dt>

*pIReader* \[ in\]
</dt> <dd>

Tipo: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _

</dd> <dt>

_pguidVendor * \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

</dd> <dt>

_ppIWriter * \[ out\]
</dt> <dd>

Tipo: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




