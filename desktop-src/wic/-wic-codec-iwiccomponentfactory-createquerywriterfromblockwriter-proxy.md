---
description: Funzione proxy per il metodo CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 44af8d96d39afff1eba582f9dea283a09acd69dbd4fc6dc95b3f568919621efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965260"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a>Funzione proxy IWICComponentFactory \_ CreateQueryWriterFromBlockWriter \_

Funzione proxy per il [**metodo CreateQueryWriterFromBlockWriter.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\***

Puntatore a [**questo oggetto IWICComponentFactory.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)

</dd> <dt>

*pIBlockWriter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\***

</dd> <dt>

*ppIQueryWriter* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




