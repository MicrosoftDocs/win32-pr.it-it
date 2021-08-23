---
description: "Metodo IWiaUIExtension::GetDeviceIcon: ottiene un'icona del dispositivo personalizzata."
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: Metodo IWiaUIExtension::GetDeviceIcon (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 040bcc6bcc5e4e8a7126c5ef7d0a72dbb688a6e5605512ff67527c21bfaa3026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813861"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Metodo IWiaUIExtension::GetDeviceIcon

Ottiene un'icona del dispositivo personalizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceId* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'ID dispositivo del dispositivo WIA per il quale è necessario ottenere l'icona.

</dd> <dt>

*phIcon* \[ Cambio\]
</dt> <dd>

Tipo: **HICON \***

Punta a una posizione di memoria che riceverà un handle per l'icona per il dispositivo.

</dd> <dt>

*nSize* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Specifica le dimensioni dell'icona desiderate, in pixel. Si presuppone che l'icona sia quadrata e che nSize specifichi sia la larghezza che l'altezza dell'icona richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




