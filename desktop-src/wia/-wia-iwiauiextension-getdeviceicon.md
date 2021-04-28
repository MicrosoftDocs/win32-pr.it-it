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
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116659"
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
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




