---
description: Funzione proxy per il metodo CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: Funzione IWICImagingFactory_CreatePalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319119"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a>IWICImagingFactory \_ CreatePalette- \_ funzione proxy

Funzione proxy per il metodo [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ in\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIPalette * \[ out\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***

Puntatore che riceve un puntatore a un nuovo [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).

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



 

 




