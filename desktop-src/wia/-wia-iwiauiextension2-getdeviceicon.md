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
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116619"
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

Se il metodo ha esito positivo, restituisce S \_ OK. Se il metodo ha esito negativo, restituisce un codice di errore appropriato. La tabella seguente illustra alcuni dei possibili codici di stato restituiti.



| Codice di errore    | Descrizione                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Il parametro bstrDeviceId o phIcon è **NULL** oppure bstrDeviceId non punta a una stringa ID dispositivo WIA valida |
| E \_ FAIL       | Nessuna risorsa icona disponibile.                                                                               |
| E \_ NOTIMPL    | Non è disponibile alcuna icona delle dimensioni richieste.                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




