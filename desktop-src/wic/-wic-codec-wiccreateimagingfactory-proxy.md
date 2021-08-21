---
description: Funzione proxy per la creazione di IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: c26ba9fbe1f230a4269fb6b71f15a39d00a80b4a3e1f19c3e5d8681e5008c5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033405"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>Funzione proxy WICCreateImagingFactory \_

Funzione proxy per la creazione [**di IWICImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)

## <a name="syntax"></a>Sintassi

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*SDKVersion* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

</dd> <dt>

*ppIImagingFactory* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione è un helper per la creazione di una factory WIC per il collegamento esplicito delle DLL, necessaria per Windows XP. Nell'utilizzo normale si usa [**invece CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (vedere class [factory dell'API WIC),](./-wic-api.md#class-factories)perché è sempre incluso in tutte le versioni più recenti di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt> </dl> |



 

