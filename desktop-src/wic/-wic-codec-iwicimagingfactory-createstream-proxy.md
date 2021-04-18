---
description: Funzione proxy per il metodo CreateStream.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Funzione IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317260"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a>IWICImagingFactory \_ CreateStream- \_ funzione proxy

Funzione proxy per il metodo [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ in\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIWICStream * \[ out\]
</dt> <dd>

Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***

Puntatore che riceve un puntatore a un nuovo [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).

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



 

 




