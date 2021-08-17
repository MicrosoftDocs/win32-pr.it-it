---
description: "Metodo IWiaUIExtension2::GetDeviceIcon: ottiene un'icona del dispositivo personalizzata."
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: Metodo IWiaUIExtension2::GetDeviceIcon (Wiadevd.h)
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
ms.openlocfilehash: 236a12bdf37a3d4c73a4601dd35667e946442bab3fc8dc66340d5f889b165f20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669383"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>Metodo IWiaUIExtension2::GetDeviceIcon

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

Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.

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

Se il metodo ha esito positivo, restituisce S \_ OK. Se il metodo ha esito negativo, restituisce un codice di errore appropriato. La tabella seguente illustra alcuni dei possibili codici di stato restituiti.



| Codice di errore    | Descrizione                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Il parametro bstrDeviceId o phIcon **è NULL** oppure bstrDeviceId non punta a una stringa di ID dispositivo WIA valida |
| E \_ FAIL       | Nessuna risorsa icona disponibile.                                                                               |
| E \_ NOTIMPL    | Non è disponibile alcuna icona delle dimensioni richieste.                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




