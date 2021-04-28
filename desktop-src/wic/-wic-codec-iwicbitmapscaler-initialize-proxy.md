---
description: IWICBitmapScaler_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100539"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a>Funzione proxy di inizializzazione IWICBitmapScaler \_ \_

Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***

Puntatore a [**questo oggetto IWICBitmapScaler.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)

</dd> <dt>

*pISource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Origine bitmap di input.

</dd> <dt>

*uiWidth* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Larghezza di destinazione.

</dd> <dt>

*uiHeight* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Altezza di desination.

</dd> <dt>

*modalità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**

Modalità di interpolazione da utilizzare per il ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, solo app desktop di Windows Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




