---
description: Esegue controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file .cab corrispondente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: Metodo IeAxiServiceCallback::VerifyFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3c8072680d42e214304cae1f0a6002b7a1fbc036fc075c5c6777dd7612733a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414711"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Metodo IeAxiServiceCallback::VerifyFile

Il **metodo VerifyFile** esegue controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file .cab corrispondente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrFileUrl* \[ Pollici\]
</dt> <dd>

URL dell'oggetto ActiveX da controllare.

</dd> <dt>

*bstrApprovedFileName* \[ Cambio\]
</dt> <dd>

Nome del file in cui è stato scaricato .cab file associato all ActiveX o object.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](/windows/desktop/SecCrypto/common-hresult-values)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

