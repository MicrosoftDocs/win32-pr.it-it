---
title: Metodo IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: Il metodo CheckCertForRevocation determina se un certificato è stato revocato.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Metodo CheckCertForRevocation Windows Media Format
- Metodo CheckCertForRevocation Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo CheckCertForRevocation
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
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325540"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>Metodo IWMDRMSecurity:: CheckCertForRevocation

Il metodo **CheckCertForRevocation** determina se un certificato è stato revocato.

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

*rguidRevocationList* \[ in\]
</dt> <dd>

GUID che identifica l'elenco di revoche da usare. Impostare su uno dei valori riportati nella tabella seguente.



| Costante GUID                 | Descrizione                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| \_app WMDRM REVOCATIONTYPE \_    | Specifica l'elenco di revoche di certificati dell'applicazione.                                     |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Specifica l'elenco di revoche di certificati del dispositivo.                                          |
| WMDRM \_ REVOCATIONTYPE \_ Cardea | Specifica l'elenco di revoche di certificati per i dispositivi di rete DRM di Microsoft Windows Media. |



 

</dd> <dt>

*pbCert* \[ in\]
</dt> <dd>

Buffer contenente il certificato da ricercare.

</dd> <dt>

*cbCert* \[ in\]
</dt> <dd>

Dimensioni del buffer *pbCert* in byte.

</dd> <dt>

*fRevoked* \[ out\]
</dt> <dd>

In output indica se il certificato è presente nell'elenco di revoche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





