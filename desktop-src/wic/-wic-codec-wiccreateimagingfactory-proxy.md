---
description: Funzione proxy per la creazione di IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Funzione WICCreateImagingFactory_Proxy
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
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313419"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>\_Funzione proxy WICCreateImagingFactory

Funzione proxy per la creazione di [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Sintassi

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*SDKVersion* \[ in\]
</dt> <dd>

Tipo: **uint**

</dd> <dt>

*ppIImagingFactory* \[ out\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione è un helper per la creazione di una factory WIC per il collegamento esplicito della DLL, necessaria per Windows XP. Nell'utilizzo normale è invece possibile utilizzare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (vedere le [class factory dell'API WIC](./-wic-api.md#class-factories)), dal momento che è sempre incluso in tutte le versioni più recenti di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>windowscodecs. lib</dt> </dl> |



 

