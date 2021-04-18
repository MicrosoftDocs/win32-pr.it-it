---
description: Ottiene un logo bitmap personalizzato per il dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Metodo IWiaUIExtension:: GetDeviceBitmapLogo (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307349"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>Metodo IWiaUIExtension:: GetDeviceBitmapLogo

Ottiene un logo bitmap personalizzato per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceId* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.

</dd> <dt>

*phBitmap* \[ out\]
</dt> <dd>

Tipo: **HBITMAP \** _

Punta a una posizione di memoria che riceverà un handle per il logo bitmap per il dispositivo.

</dd> <dt>

_nMaxWidth * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica la larghezza desiderata della bitmap.

</dd> <dt>

*nMaxHeight* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica l'altezza desiderata della bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




