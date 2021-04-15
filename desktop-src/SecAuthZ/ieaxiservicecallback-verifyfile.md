---
description: Esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Metodo IeAxiServiceCallback:: VerifyFile'
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
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529880"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Metodo IeAxiServiceCallback:: VerifyFile

Il metodo **VerifyFile** esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrFileUrl* \[ in\]
</dt> <dd>

URL dell'oggetto ActiveX da verificare.

</dd> <dt>

*bstrApprovedFileName* \[ out\]
</dt> <dd>

Nome del file in cui è stato scaricato il file con estensione cab associato all'oggetto ActiveX.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

