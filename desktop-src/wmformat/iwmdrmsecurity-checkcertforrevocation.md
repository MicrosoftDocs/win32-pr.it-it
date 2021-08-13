---
title: Metodo IWMDRMSecurity CheckCertForRevocation (Wmdrmsdk.h)
description: Il metodo CheckCertForRevocation determina se un certificato è stato revocato.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Metodo CheckCertForRevocation in formato Windows Media
- Metodo CheckCertForRevocation windows Media Format , interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity windows Media Format , metodo CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e090dfb655837ad2cf36cf45486488fde1440b499b73f16fdfbdaf2989532687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700787"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>Metodo IWMDRMSecurity::CheckCertForRevocation

Il **metodo CheckCertForRevocation** determina se un certificato è stato revocato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rguidRevocationList* \[ Pollici\]
</dt> <dd>

GUID che identifica l'elenco di revoche da usare. Impostare su uno dei valori nella tabella seguente.



| Costante GUID                 | Descrizione                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ APP    | Specifica l'elenco di revoche di certificati dell'applicazione.                                     |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Specifica l'elenco di revoche di certificati del dispositivo.                                          |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Specifica l'elenco di revoche di certificati di Microsoft Windows Media DRM per dispositivi di rete. |



 

</dd> <dt>

*pbCert* \[ Pollici\]
</dt> <dd>

Buffer contenente il certificato da cercare.

</dd> <dt>

*cbCert* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *pbCert,* in byte.

</dd> <dt>

*fRevoked* \[ Cambio\]
</dt> <dd>

Nell'output indica se il certificato è presente nell'elenco di revoche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





