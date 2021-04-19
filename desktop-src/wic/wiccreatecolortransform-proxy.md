---
description: Crea un oggetto di trasformazione colore che implementa IWICColorTransform. Questo oggetto COM supporta il modello a oggetti a thread libero.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Funzione WICCreateColorTransform_Proxy
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
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325697"
---
# <a name="wiccreatecolortransform_proxy-function"></a>\_Funzione proxy WICCreateColorTransform

Crea un oggetto di trasformazione colore che implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Questo oggetto COM supporta il modello a oggetti a thread libero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIColorTransform* \[ out\]
</dt> <dd>

Trasformazione colore creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
