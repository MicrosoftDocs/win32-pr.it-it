---
description: Crea un oggetto di trasformazione del colore che implementa IWICColorTransform. Questo oggetto COM supporta il modello a oggetti a thread libero.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 89c7476bc32546f0a9fe77a8731f239702c6a2a874dbfb830b9d4bbafbd872b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709218"
---
# <a name="wiccreatecolortransform_proxy-function"></a>Funzione proxy WICCreateColorTransform \_

Crea un oggetto di trasformazione del colore che implementa [**IWICColorTransform.**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform) Questo oggetto COM supporta il modello a oggetti a thread libero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIColorTransform* \[ Cambio\]
</dt> <dd>

Trasformazione del colore creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
