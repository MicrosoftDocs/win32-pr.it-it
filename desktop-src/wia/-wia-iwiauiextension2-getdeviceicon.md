---
description: Ottiene un'icona di dispositivo personalizzata.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'Metodo IWiaUIExtension2:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526443"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>Metodo IWiaUIExtension2:: GetDeviceIcon

Ottiene un'icona di dispositivo personalizzata.

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

*bstrDeviceId* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \** _

Punta a una posizione di memoria che riceverà un handle per l'icona del dispositivo.

</dd> <dt>

_nSize * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica la dimensione dell'icona desiderata, in pixel. Si presuppone che l'icona sia quadrata, mentre nSize specifica sia la larghezza che l'altezza dell'icona richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce S \_ OK. Se il metodo ha esito negativo, viene restituito un codice di errore appropriato. Nella tabella seguente vengono illustrati alcuni dei possibili codici di stato restituiti.



| Codice di errore    | Descrizione                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Il parametro bstrDeviceId o phIcon è **null** oppure bstrDeviceId non punta a una stringa di ID del dispositivo WIA valida |
| E \_ non riescono       | Non sono disponibili risorse icona.                                                                               |
| E \_ NOTIMPL    | Non è disponibile alcuna icona delle dimensioni richieste.                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




